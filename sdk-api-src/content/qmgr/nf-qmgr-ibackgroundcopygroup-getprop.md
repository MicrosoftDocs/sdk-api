---
UID: NF:qmgr.IBackgroundCopyGroup.GetProp
title: IBackgroundCopyGroup::GetProp
author: windows-sdk-content
description: Use the GetProp method to retrieve a property value from the group.
old-location: bits\ibackgroundcopygroup_getprop.htm
tech.root: Bits
ms.assetid: c27debdf-22eb-417e-b870-2891167f4498
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetProp, GetProp method [BITS], GetProp method [BITS],IBackgroundCopyGroup interface, IBackgroundCopyGroup interface [BITS],GetProp method, IBackgroundCopyGroup.GetProp, IBackgroundCopyGroup::GetProp, bits.ibackgroundcopygroup_getprop, qmgr/IBackgroundCopyGroup::GetProp
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyGroup.GetProp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyGroup::GetProp


## -description


<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>GetProp</b> method to retrieve a property value from the group.


## -parameters




### -param propID

TBD


### -param pvarVal

TBD




#### - PropId [in]

Identifies the property to retrieve. For a list of properties, see the <a href="https://msdn.microsoft.com/8bd5d1df-237a-4c42-afe1-6540ab1ad8c1">GROUPPROP</a> enumeration.


#### - pvarPropValue [out]

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
Successfully retrieved the property.

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
 

 

