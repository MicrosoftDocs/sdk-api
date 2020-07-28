---
UID: NF:mfobjects.IMFAttributes.GetUnknown
title: IMFAttributes::GetUnknown (mfobjects.h)
description: Retrieves an interface pointer associated with a key.
helpviewer_keywords: ["GetUnknown","GetUnknown method [Media Foundation]","GetUnknown method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","GetUnknown method","IMFAttributes.GetUnknown","IMFAttributes::GetUnknown","a5f645a1-b7d2-47d3-b77e-ad94815b1c25","mf.imfattributes_getunknown","mfobjects/IMFAttributes::GetUnknown"]
old-location: mf\imfattributes_getunknown.htm
tech.root: mf
ms.assetid: a5f645a1-b7d2-47d3-b77e-ad94815b1c25
ms.date: 12/05/2018
ms.keywords: GetUnknown, GetUnknown method [Media Foundation], GetUnknown method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetUnknown method, IMFAttributes.GetUnknown, IMFAttributes::GetUnknown, a5f645a1-b7d2-47d3-b77e-ad94815b1c25, mf.imfattributes_getunknown, mfobjects/IMFAttributes::GetUnknown
f1_keywords:
- mfobjects/IMFAttributes.GetUnknown
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
- IMFAttributes.GetUnknown
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFAttributes::GetUnknown


## -description



Retrieves an interface pointer associated with a key.




## -parameters




### -param guidKey [in]

GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_IUNKNOWN</b>.


### -param riid [in]

Interface identifier (IID) of the interface to retrieve.


### -param ppv [out]

Receives a pointer to the requested interface. The caller must release the interface.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The attribute value is an <b>IUnknown</b> pointer but does not support requested interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified key was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDTYPE</b></dt>
</dl>
</td>
<td width="60%">
The attribute value is not an <b>IUnknown</b> pointer.

</td>
</tr>
</table>
 




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type">MF_ATTRIBUTE_TYPE</a>
 

 

