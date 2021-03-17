---
UID: NF:shobjidl_core.IShellItemArray.GetAttributes
title: IShellItemArray::GetAttributes (shobjidl_core.h)
description: Gets the attributes of the set of items contained in an IShellItemArray.
helpviewer_keywords: ["GetAttributes","GetAttributes method [Windows Shell]","GetAttributes method [Windows Shell]","IShellItemArray interface","IShellItemArray interface [Windows Shell]","GetAttributes method","IShellItemArray.GetAttributes","IShellItemArray::GetAttributes","SIATTRIBFLAGS_ALLITEMS","SIATTRIBFLAGS_AND","SIATTRIBFLAGS_APPCOMPAT","SIATTRIBFLAGS_MASK","SIATTRIBFLAGS_OR","_shell_IShellItemArray_GetAttributes","shell.IShellItemArray_GetAttributes","shobjidl_core/IShellItemArray::GetAttributes"]
old-location: shell\IShellItemArray_GetAttributes.htm
tech.root: shell
ms.assetid: 0498ce03-9949-48bb-a1eb-b569f4171884
ms.date: 12/05/2018
ms.keywords: GetAttributes, GetAttributes method [Windows Shell], GetAttributes method [Windows Shell],IShellItemArray interface, IShellItemArray interface [Windows Shell],GetAttributes method, IShellItemArray.GetAttributes, IShellItemArray::GetAttributes, SIATTRIBFLAGS_ALLITEMS, SIATTRIBFLAGS_AND, SIATTRIBFLAGS_APPCOMPAT, SIATTRIBFLAGS_MASK, SIATTRIBFLAGS_OR, _shell_IShellItemArray_GetAttributes, shell.IShellItemArray_GetAttributes, shobjidl_core/IShellItemArray::GetAttributes
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellItemArray::GetAttributes
 - shobjidl_core/IShellItemArray::GetAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellItemArray.GetAttributes
---

# IShellItemArray::GetAttributes


## -description

Gets the attributes of the set of items contained in an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>. If the array contains more than one item, the attributes retrieved by this method are not the attributes of single items, but a logical combination of all of the requested attributes of all of the items.

## -parameters

### -param AttribFlags [in]

Type: <b>SIATTRIBFLAGS</b>

If the array contains a single item, this method provides the same results as <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getattributes">GetAttributes</a>. However, if the array contains multiple items, the attribute sets of all the items are combined into a single attribute set and returned in the value pointed to by <i>psfgaoAttribs</i>. This parameter takes one of the following values to define how that final attribute set is determined:



#### SIATTRIBFLAGS_AND (0x00000001)

0x00000001. If there are multiple items in the array, use a bitwise AND to combine the attributes across items. For instance, if the array contains two items where one item can be moved (SFGAO_CANMOVE) and a second item cannot, the method returns (1 &amp; 0) or 0 for that attribute bit.



#### SIATTRIBFLAGS_OR (0x00000002)

0x00000002. If there are multiple items in the array, use a bitwise OR to combine the attributes across items. For instance, if the array contains two items where one item can be moved (SFGAO_CANMOVE) and a second item cannot, the method returns (1 | 0) or 1 for that attribute bit.



#### SIATTRIBFLAGS_APPCOMPAT (0x00000003)

0x00000003. Retrieve the attributes directly from the Shell data source. To use this value, the Shell item array must have been initialized as an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> with its contents specified as an array of child PIDLs.



#### SIATTRIBFLAGS_MASK (0x00000003)

0x00000003. A mask for SIATTRIBFLAGS_AND, SIATTRIBFLAGS_OR, and SIATTRIBFLAGS_APPCOMPAT. Callers normally do not use this value.



#### SIATTRIBFLAGS_ALLITEMS (0x00004000)

0x00004000. <b>Windows 7 and later</b>. Examine all items in the array to compute the attributes. Note that this can result in poor performance over large arrays and therefore it should be used only when needed. Cases in which you pass this flag should be extremely rare. See Remarks for more details.

### -param sfgaoMask [in]

Type: <b>SFGAOF</b>

A mask that specifies what particular attributes are being requested. A bitwise OR of one or more of the <a href="/windows/desktop/shell/sfgao">SFGAO</a> values.

### -param psfgaoAttribs [out]

Type: <b>SFGAOF*</b>

A bitmap that, when this method returns successfully, contains the values of the requested attributes.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the attributes returned exactly match those requested in <i>sfgaoMask</i>, S_FALSE if the attributes do not exactly match, or a standard COM error value otherwise.

## -remarks

The Shell item array caches individual attributes after they have been determined.

As this method passes through the array gathering attribute information, it normally stops looking at a particular attribute after that value is irrevocably set. For instance, if the SIATTRIBFLAGS_AND flag is set, after an attribute is found not to be set on an item (a value of 0), there is no need to continue examining that attribute value on other items because the result of the AND operation will always be 0. Therefore, the final set of attributes is commonly calculated by looking at only the first few items in the array, which is all that is needed to obtain the final value. If you have a need to examine all items in the array, set the SIATTRIBFLAGS_ALLITEMS flag. However, be aware that this can slow the method's return considerably, so do not do so without cause.