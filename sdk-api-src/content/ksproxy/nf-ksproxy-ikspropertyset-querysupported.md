---
UID: NF:ksproxy.IKsPropertySet.QuerySupported
title: IKsPropertySet::QuerySupported method
author: windows-driver-content
description: The QuerySupported method determines whether an object supports a specified property set.
old-location: dshow\ikspropertyset_querysupported.htm
old-project: DirectShow
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IKsPropertySet, IKsPropertySet interface [DirectShow], QuerySupported method, IKsPropertySet::QuerySupported, IKsPropertySetQuerySupported, QuerySupported method [DirectShow], QuerySupported method [DirectShow], IKsPropertySet interface, QuerySupported,IKsPropertySet.QuerySupported, dshow.ikspropertyset_querysupported, ks/IKsPropertySet::QuerySupported, ksproxy/IKsPropertySet::QuerySupported
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ksproxy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WAVEFORMATEXTENSIBLE, *PWAVEFORMATEXTENSIBLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IKsPropertySet.QuerySupported
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKsPropertySet::QuerySupported method


## -description



The <code>QuerySupported</code> method determines whether an object supports a specified property set.




## -parameters




### -param PropSet




### -param Id




### -param TypeSupport






#### - dwPropID [in]

Identifier of the property within the property set.


#### - guidPropSet [in]

Property set GUID.


#### - pTypeSupport [out]

Pointer to a value in which to store flags indicating the support provided by the driver. Supported flags include the following.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>KSPROPERTY_SUPPORT_GET</td>
<td>You can retrieve the property by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff560719">IKsPropertySet::Get</a> method.</td>
</tr>
<tr>
<td>KSPROPERTY_SUPPORT_SET</td>
<td>You can change the property by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff560721">IKsPropertySet::Set</a>.</td>
</tr>
</table>
 


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
The specified property set and property ID combination is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Property set is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PROP_ID_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Property ID is not supported for the specified property set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PROP_SET_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Property set is not supported.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  Another interface by this name exists in the dsound.h header file. The two interfaces are not compatible. The <b>IKsControl</b> interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</div>
<div> </div>
You must include Ks.h before Ksproxy.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/df26341d-f2d5-4a4e-954e-705e07415808">IKsPropertySet Interface</a>



<a href="https://msdn.microsoft.com/4b8a917f-7a6c-4433-83f4-b83ef6d26115">Property Sets</a>
 

 

