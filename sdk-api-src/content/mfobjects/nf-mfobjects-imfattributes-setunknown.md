---
UID: NF:mfobjects.IMFAttributes.SetUnknown
title: IMFAttributes::SetUnknown (mfobjects.h)
description: Associates an IUnknown pointer with a key.
old-location: mf\imfattributes_setunknown.htm
tech.root: medfound
ms.assetid: da0c3d59-07c4-4431-a137-8655ddbf6258
ms.date: 12/05/2018
ms.keywords: IMFAttributes interface [Media Foundation],SetUnknown method, IMFAttributes.SetUnknown, IMFAttributes::SetUnknown, SetUnknown, SetUnknown method [Media Foundation], SetUnknown method [Media Foundation],IMFAttributes interface, da0c3d59-07c4-4431-a137-8655ddbf6258, mf.imfattributes_setunknown, mfobjects/IMFAttributes::SetUnknown
ms.topic: method
f1_keywords:
- mfobjects/IMFAttributes.SetUnknown
dev_langs:
- c++
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFAttributes.SetUnknown
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFAttributes::SetUnknown


## -description



Associates an <b>IUnknown</b> pointer with a key.




## -parameters




### -param guidKey [in]

GUID that identifies the value to set. If this key already exists, the method overwrites the old value.


### -param pUnknown [in]

<b>IUnknown</b> pointer to be associated with this key.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



To retrieve the <b>IUnknown</b> pointer, call <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown">IMFAttributes::GetUnknown</a>.

It is not an error to call <b>SetUnknown</b> with <i>pUnknown</i> equal to <b>NULL</b>. However, <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown">GetUnknown</a> will return <b>MF_E_INVALIDTYPE</b>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>
 

 

