---
UID: NN:ksproxy.IKsPropertySet
title: IKsPropertySet
author: windows-driver-content
description: The IKsPropertySet interface was originally designed as an efficient way to set and retrieve device properties on WDM drivers, using KSProxy to translate the user-mode COM method calls into the kernel-mode property sets used by WDM streaming class drivers. This interface is now also used to pass information strictly between software components.In some cases, software components must implement either this interface, or else the IKsControl interface (documented in the DirectShow DDK). For example, if you are writing a software MPEG-2 decoder for use with the DVD Navigator, you must implement one of these interfaces and also support the DVD-related property sets that the Navigator will send to the decoder. Pins may support one of these interfaces to allow other pins or filters to set or retrieve their properties.Note  Another interface by this name exists in the dsound.h header file. The two interfaces are not compatible. The IKsControl interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components. .
old-location: dshow\ikspropertyset.htm
old-project: DirectShow
ms.assetid: df26341d-f2d5-4a4e-954e-705e07415808
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IKsPropertySet, IKsPropertySet interface [DirectShow], IKsPropertySet interface [DirectShow], described, IKsPropertySetInterface, dshow.ikspropertyset, ksproxy/IKsPropertySet
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IKsPropertySet
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKsPropertySet interface


## -description



The <code>IKsPropertySet</code> interface was originally designed as an efficient way to set and retrieve device properties on WDM drivers, using KSProxy to translate the user-mode COM method calls into the kernel-mode property sets used by WDM streaming class drivers. This interface is now also used to pass information strictly between software components.

In some cases, software components must implement either this interface, or else the <b>IKsControl</b> interface (documented in the DirectShow DDK). For example, if you are writing a software MPEG-2 decoder for use with the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a>, you must implement one of these interfaces and also support the DVD-related property sets that the Navigator will send to the decoder. Pins may support one of these interfaces to allow other pins or filters to set or retrieve their properties.

<div class="alert"><b>Note</b>  Another interface by this name exists in the dsound.h header file. The two interfaces are not compatible. The <b>IKsControl</b> interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IKsPropertySet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IKsPropertySet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IKsPropertySet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>
</td>
<td align="left" width="63%">
Retrieves a property identified by a property set GUID and a property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eda0325c-dba4-4d9f-81e2-7fd67d5b9873">QuerySupported</a>
</td>
<td align="left" width="63%">
Determines whether an object supports a specified property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff544503">Set</a>
</td>
<td align="left" width="63%">
Sets a property identified by a property set GUID and a property ID.

</td>
</tr>
</table> 


## -remarks



You must include Ks.h before Ksproxy.h.




## -see-also




<a href="https://msdn.microsoft.com/4b8a917f-7a6c-4433-83f4-b83ef6d26115">Property Sets</a>
 

 

