---
UID: NS:mmc._SCOPEDATAITEM
title: SCOPEDATAITEM (mmc.h)
description: The SCOPEDATAITEM structure specifies items to be inserted into the scope pane.
helpviewer_keywords: ["*LPSCOPEDATAITEM","LPSCOPEDATAITEM","LPSCOPEDATAITEM structure pointer [MMC]","SCOPEDATAITEM","SCOPEDATAITEM structure [MMC]","SDI_CHILDREN","SDI_FIRST","SDI_IMAGE","SDI_NEXT","SDI_OPENIMAGE","SDI_PARAM","SDI_PARENT","SDI_PREVIOUS","SDI_STATE","SDI_STR","_slate_scopedataitem","mmc.scopedataitem","mmc/LPSCOPEDATAITEM","mmc/SCOPEDATAITEM"]
old-location: mmc\scopedataitem.htm
tech.root: mmc
ms.assetid: c392f25c-80e7-4c91-9063-36143320b9aa
ms.date: 12/05/2018
ms.keywords: '*LPSCOPEDATAITEM, LPSCOPEDATAITEM, LPSCOPEDATAITEM structure pointer [MMC], SCOPEDATAITEM, SCOPEDATAITEM structure [MMC], SDI_CHILDREN, SDI_FIRST, SDI_IMAGE, SDI_NEXT, SDI_OPENIMAGE, SDI_PARAM, SDI_PARENT, SDI_PREVIOUS, SDI_STATE, SDI_STR, _slate_scopedataitem, mmc.scopedataitem, mmc/LPSCOPEDATAITEM, mmc/SCOPEDATAITEM'
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SCOPEDATAITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SCOPEDATAITEM
 - mmc/_SCOPEDATAITEM
 - SCOPEDATAITEM
 - mmc/SCOPEDATAITEM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - SCOPEDATAITEM
---

# SCOPEDATAITEM structure


## -description

The 
<b>SCOPEDATAITEM</b> structure specifies items to be inserted into the scope pane.

## -struct-fields

### -field mask

A value that specifies an array of flags  that indicate  which members of the structure contain valid data. When this structure is used in the 
<a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-getitem">IConsoleNameSpace2::GetItem</a> method, it indicates the item attributes to be retrieved. This member can be one of the following values.



#### SDI_STR (0x00002)

The <b>displayname</b> member of the structure is valid. <b>SDI_STR</b> is supported only when  you specify a value for the <b>displayname</b> member. MMC does not store the value for the <b>displayname</b> member, and it cannot be retrieved by calling the <a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-getitem">IConsoleNamespace2::GetItem</a> method.



#### SDI_IMAGE (0x00004)

The <b>nImage</b> member of the structure is valid or must be filled in.



#### SDI_OPENIMAGE (0x00008)

The <b>nOpenImage</b> member of the structure is valid or must be filled in.



#### SDI_STATE (0x00010)

The <b>nState</b> member of the structure is valid or must be filled in.



#### SDI_PARAM (0x00020)

The <b>lParam</b> member of the structure is valid or must be filled in.



#### SDI_CHILDREN (0x00040)

The <b>cChildren</b> member of the structure is valid or must be filled in.



#### SDI_PARENT (0x00000000)

Use only when inserting items into the scope pane. The <b>relativeID</b> member of the structure is the <b>HSCOPEITEM</b> of the parent. The item  is  inserted as the last child of the item referred to by <b>relativeID</b>.



#### SDI_PREVIOUS (0x10000000)

Use only when inserting items into the scope pane. The <b>relativeID</b> member of the structure is the <b>HSCOPEITEM</b> of the previous sibling.



#### SDI_NEXT (0x20000000)

Use only when inserting items into the scope pane. The <b>relativeID</b> member of the structure is the <b>HSCOPEITEM</b> of the next sibling.



#### SDI_FIRST (0x08000000)

Use only when inserting items into the scope pane. The <b>relativeID</b> member of the structure is the <b>HSCOPEITEM</b> of the parent. The item  is  inserted as the first child of the item referred to by <b>relativeID</b>.

### -field displayname

<b>MMC_CALLBACK</b> value or a pointer to a null-terminated string, which depends on how the structure is being used.

<ul>
<li>When an item is inserted  by using 
<a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-insertitem">IConsoleNameSpace2::InsertItem</a>, this member must be set to <b>MMC_CALLBACK</b>.</li>
<li>When the name of an item inserted by the snap-in is changed  by using 
<a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-setitem">IConsoleNameSpace2::SetItem</a>, this member must be set to <b>MMC_CALLBACK</b>.</li>
<li>When the name of the static node (an item  that the console inserts) is changed, this member can  be set to <b>MMC_CALLBACK</b>, or be a pointer to the null-terminated string that contains the item text.</li>
</ul>
Be aware that the snap-in can use <b>MMC_TEXTCALLBACK</b> instead of <b>MMC_CALLBACK</b>. The <b>MMC_TEXTCALLBACK</b> value is a type-correct (no casting necessary) version of <b>MMC_CALLBACK</b>.

<b>MMC_TEXTCALLBACK</b> is introduced in MMC version 1.2.

### -field nImage

Virtual image index in the image list when the item is in the nonselected state. Be aware that the virtual image index is mapped internally to the actual index. This member can also be specified as a callback item: <b>MMC_CALLBACK</b> or <b>MMC_IMAGECALLBACK</b>. The <b>MMC_IMAGECALLBACK</b> is a type-correct (no casting necessary) version of <b>MMC_CALLBACK</b>.

<b>MMC_IMAGECALLBACK</b> is introduced in MMC version 1.2.

### -field nOpenImage

Virtual image index in the image list when the item is in the selected state. Be aware that the virtual image index is mapped internally to the actual index. The item is like a folder in Microsoft Windows Explorer. The icon is for an open folder.

### -field nState

A value that specifies the state mask for the item. For <a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-getitem">IConsoleNameSpace2::GetItem</a>, this member returns <b>MMC_SCOPE_ITEM_STATE_EXPANDEDONCE</b> if the item has been expanded at least  one time,  or 0 (zero) if the item has not been expanded.

This member is ignored for <a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-insertitem">IConsoleNameSpace2::InsertItem</a> and <a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-setitem">IConsoleNameSpace2::SetItem</a>.

### -field cChildren

A value that specifies the number of enumerated items.

When a snap-in inserts a scope item, it should set the <b>cChildren</b> field to  0 (zero),  and set the <b>SDI_CHILDREN</b> flag if both of the following conditions are met:

<ul>
<li>The snap-in does not have any child items to add under the inserted item.</li>
<li>The snap-in does not dynamically enable any namespace extension snap-ins for this item.</li>
</ul>
Otherwise, when inserting a scope item, the <b>cChildren</b> field should be set to 1 (one), or not set at all.

If conditions change at a later time, the snap-in can modify the <b>cChildren</b> field  by using 
<a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-setitem">IConsoleNameSpace2::SetItem</a>.

If  it  will take a significant amount of time to determine the number of children, the snap-in should use a best guess at insertion time, and make the actual determination on another thread so the MMC user interface will not be locked out. 
<a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-setitem">IConsoleNameSpace2::SetItem</a> can be used to correct the setting if necessary.

When MMC detects a scope item with a <b>cChildren</b> count of 0 (zero), it  checks for   namespace extensions  that have been statically enabled for the item  by the user or  the 
<a href="/windows/desktop/api/mmc/nn-mmc-irequiredextensions">IRequiredExtensions</a> interface. If none are enabled, the plus (+) sign  is  removed from the item.

After an item  is  expanded, the state of the plus sign  is  determined by the actual number of child items present.

### -field lParam

A value that specifies a user-supplied 32-bit value to associate with the item. This item, also called a cookie, is the value that is passed as the first parameter to 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponentdata-querydataobject">IComponentData::QueryDataObject</a>.

### -field relativeID

A console-supplied unique item identifier. An item is inserted at a position relative to the item  that  this member specifies. The  <b>mask</b> settings determine the  relative position.

To determine how <b>relativeID</b> is interpreted, specify one of the following constants as the <b>mask</b> member.



#### SDI_PARENT

<b>relativeID</b> is the <b>HSCOPEITEM</b> of the parent. The item is inserted as the last child of the parent item. The value of <b>SDI_PARENT</b> indicates  that it is a no-op, because by default,  the parent item  ID  is <b>relativeID</b>.



#### SDI_PREVIOUS

<b>relativeID</b> is the <b>HSCOPEITEM</b> of the previous sibling.



#### SDI_NEXT

<b>relativeID</b> is the <b>HSCOPEITEM</b> of the next sibling.



#### SDI_FIRST

Same as <b>SDI_PARENT</b>, except  the item is inserted as the first child.

### -field ID

A value that specifies a console-supplied unique identifier for the scope item. This value is used to identify an item in the scope pane  of  calls to  some  of the 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a> and 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace2">IConsoleNameSpace2</a> interface methods.

After the snap-in successfully inserts an item into the scope pane (by using <a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-insertitem">IConsoleNameSpace2::InsertItem</a>), the 
<b>ID</b> member of the 
<b>SCOPEDATAITEM</b> structure contains the <b>HSCOPEITEM</b> handle of the newly inserted item. This handle is the unique identifier for the scope item.

For a  static node, MMC  inserts  an item  into the  scope pane  of the snap-in. Then  MMC  passes the  <b>HSCOPEITEM</b>  of the  static node  to the snap-in as the <i>param</i> parameter in the <a href="/previous-versions/windows/desktop/mmc/mmcn-expand">MMCN_EXPAND</a> notification.

Be aware that snap-ins should store the <b>HSCOPEITEM</b> of each inserted item and use it  later  to  manipulate the item  by using the methods of the 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a> and 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace2">IConsoleNameSpace2</a> interfaces.

## -remarks

It is not valid to insert an item as a sibling of the static node. If a snap-in sets the <b>relativeID</b> member to the <b>HSCOPEITEM</b> of the static node, sets  the <b>SDI_PREVIOUS</b> or <b>SDI_NEXT</b> flags, and then calls <a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-insertitem">IConsoleNameSpace2::InsertItem</a>, MMC  returns  <b>E_INVALIDARG</b>.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>



<a href="/windows/desktop/api/mmc/nf-mmc-icomponentdata-getdisplayinfo">IComponentData::GetDisplayInfo</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-getitem">IConsoleNameSpace2::GetItem</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-insertitem">IConsoleNameSpace2::InsertItem</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-setitem">IConsoleNameSpace2::SetItem</a>