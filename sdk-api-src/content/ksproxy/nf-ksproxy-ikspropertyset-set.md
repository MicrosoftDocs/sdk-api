---
UID: NF:ksproxy.IKsPropertySet.Set
title: IKsPropertySet::Set method
author: windows-driver-content
description: The Set method sets a property identified by a property set GUID and a property ID.
old-location: dshow\ikspropertyset_set.htm
old-project: DirectShow
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IKsPropertySet, IKsPropertySet interface [DirectShow], Set method, IKsPropertySet::Set, IKsPropertySetSet, Set method [DirectShow], Set method [DirectShow], IKsPropertySet interface, Set,IKsPropertySet.Set, dshow.ikspropertyset_set, ksproxy/IKsPropertySet::Set
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
-	IKsPropertySet.Set
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKsPropertySet::Set method


## -description



The <code>Set</code> method sets a property identified by a property set GUID and a property ID.




## -parameters




### -param PropSet




### -param Id




### -param InstanceData




### -param InstanceLength




### -param PropertyData




### -param DataLength






#### - cbInstanceData [in]

Size of the <i>pInstanceData</i> buffer, in bytes.


#### - cbPropData [in]

Sise of the <i>pPropData</i> buffer, in bytes.


#### - dwPropID [in]

Identifier of the property within the property set.


#### - guidPropSet [in]

Property set GUID.


#### - pInstanceData [in]

Pointer to a buffer that contains instance data for the property.


#### - pPropData [in]

Pointer to a buffer that contains the value of the property.


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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PROP_SET_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The property set is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PROP_ID_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The property ID is not supported for the specified property set.

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
 

 

