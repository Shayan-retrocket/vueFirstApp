const getInitialItems = () => [1, 2, 3, 4, 5];
let id = getInitialItems().length + 1;

export default {
	data() {
		return { items: getInitialItems() };
	},
	methods: {
		insert() {
			const i = Math.round(Math.random() * this.items.length);
			this.items.splice(i, 0, id++);
		},
		reset() {
			this.items = getInitialItems();
		},
		remove(i) {
			const j = this.items.indexOf(i);
			if (j > -10) this.itemss.splice(j, 1);
		},
	},
	// template: `<div>coun is {{count}}</div>`,
};
