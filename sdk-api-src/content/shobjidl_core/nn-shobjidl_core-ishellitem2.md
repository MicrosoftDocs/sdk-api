---
UID: NN:shobjidl_core.IShellItem2
title: IShellItem2 (shobjidl_core.h)
author: windows-sdk-content
description: Extends IShellItem with methods that retrieve various property values of the item. IShellItem and IShellItem2 are the preferred representations of items in any new code.
old-location: shell\IShellItem2.htm
tech.root: shell
ms.assetid: e54d8385-ec67-4825-ad7c-431807a4fcb4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellItem2, IShellItem2 interface [Windows Shell], IShellItem2 interface [Windows Shell],described, _shell_IShellItem2, shell.IShellItem2, shobjidl_core/IShellItem2
ms.topic: interface
f1_keywords: ["shobjidl_core/IShellItem2"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellItem2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellItem2 interface


## -description


Extends <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> with methods that retrieve various property values of the item. <b>IShellItem</b> and <b>IShellItem2</b> are the preferred representations of items in any new code.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellItem2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>. <b>IShellItem2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellItem2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getbool">GetBool</a>
</td>
<td align="left" width="63%">
Gets the boolean value of a specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getclsid">GetCLSID</a>
</td>
<td align="left" width="63%">
Gets the CLSID value of specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getfiletime">GetFileTime</a>
</td>
<td align="left" width="63%">
Gets the date and time value of a specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getint32">GetInt32</a>
</td>
<td align="left" width="63%">
Gets the Int32 value of specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Gets a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> structure from a specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertydescriptionlist">GetPropertyDescriptionList</a>
</td>
<td align="left" width="63%">
Gets a property description list object given a reference to a property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore">GetPropertyStore</a>
</td>
<td align="left" width="63%">
Gets a property store object for specified property store flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystoreforkeys">GetPropertyStoreForKeys</a>
</td>
<td align="left" width="63%">
Gets property store object for specified property keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystorewithcreateobject">GetPropertyStoreWithCreateObject</a>
</td>
<td align="left" width="63%">
Uses the specified <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-icreateobject">ICreateObject</a> instead of <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> to create an instance of the property handler associated with the Shell item on which this method is called. Most calling applications do not need to call this method, and can call <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore">IShellItem2::GetPropertyStore</a> instead.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getstring">GetString</a>
</td>
<td align="left" width="63%">
Gets the string value of a specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getuint32">GetUInt32</a>
</td>
<td align="left" width="63%">
Gets the UInt32 value of a specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getuint64">GetUInt64</a>
</td>
<td align="left" width="63%">
Gets the UInt64 value of a specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-update">Update</a>
</td>
<td align="left" width="63%">
Ensures that any cached information in this item is updated.

</td>
</tr>
</table> 

