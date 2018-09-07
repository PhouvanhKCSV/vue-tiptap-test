<template>
  <editor :extensions="extensions">
    <div slot="content" slot-scope="props">
      <h1>Yay Headlines!</h1>
      <p>All these <strong>cool tags</strong> are working now.</p>
    </div>
  </editor>
</template>

<script>
import { Editor } from 'tiptap/dist/tiptap.esm.js'
import {
  // Nodes
  BlockquoteNode,
  BulletListNode,
  HardBreakNode,
  HeadingNode,
  ImageNode,
  ListItemNode,
  OrderedListNode,

  // Marks
  BoldMark,
  ItalicMark,
  LinkMark,
  StrikeMark,

  // General Extensions
  PlaceholderExtension,
} from 'tiptap-extensions/dist/extensions.esm.js'

export default {
  components: {
    Editor,
  },
  data() {
    return {
      extensions: [
        new BlockquoteNode(),
        new BulletListNode(),
        new HardBreakNode(),
        new HeadingNode({ maxLevel: 3 }),
        new ImageNode(),
        new ListItemNode(),
        new OrderedListNode(),
        new BoldMark(),
        new ItalicMark(),
        new LinkMark(),
        new StrikeMark(),
        new PlaceholderExtension(),
      ],
    }
  },
}
</script>
