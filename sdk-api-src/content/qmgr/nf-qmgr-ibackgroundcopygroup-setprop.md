---
UID: NF:qmgr.IBackgroundCopyGroup.SetProp
title: IBackgroundCopyGroup::SetProp
author: windows-sdk-content
description: Use the SetProp method to set the property value for a group property.
old-location: bits\ibackgroundcopygroup_setprop.htm
old-project: Bits
ms.assetid: 057a1004-fbe6-4c90-84c0-4e5b55539ce9
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IBackgroundCopyGroup interface [BITS],SetProp method, IBackgroundCopyGroup.SetProp, IBackgroundCopyGroup::SetProp, SetProp, SetProp method [BITS], SetProp method [BITS],IBackgroundCopyGroup interface, bits.ibackgroundcopygroup_setprop, qmgr/IBackgroundCopyGroup::SetProp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: GROUPPROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyGroup.SetProp
product: Windows
targetos: Windows
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
req.product: ADAM
---

# IBackgroundCopyGroup::SetProp


## -description


<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>SetProp</b> method to set the property value for a group property.


## -parameters




### -param propID




### -param pvarVal






#### - PropId [in]

Identifies the property to set. For a list of properties, see the <a href="https://msdn.microsoft.com/8bd5d1df-237a-4c42-afe1-6540ab1ad8c1">GROUPPROP</a> enumeration.


#### - pvarPropValue [in]

Property value.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully set the property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
You specified a property that is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
You specified a variant type that is not compatible with the property.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/51ddd89a-489a-4b83-ad45-838809a6d2e8">IBackgroundCopyGroup</a>
 

 

