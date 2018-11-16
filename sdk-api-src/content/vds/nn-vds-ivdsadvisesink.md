---
UID: NN:vds.IVdsAdviseSink
title: IVdsAdviseSink
author: windows-sdk-content
description: Receives VDS notifications.
old-location: base\ivdsadvisesink.htm
tech.root: VDS
ms.assetid: 8e9b7c95-0b59-4268-a274-5d16812075a6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IVdsAdviseSink, IVdsAdviseSink interface [VDS], IVdsAdviseSink interface [VDS],described, base.ivdsadvisesink, vds/IVdsAdviseSink, vdshwprv/IVdsAdviseSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsAdviseSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsAdviseSink interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Receives VDS 
   notifications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsAdviseSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsAdviseSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsAdviseSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0cf7bf55-922e-4092-bb2f-6423d9addb0c">OnNotify</a>
</td>
<td align="left" width="63%">
Passes notifications from providers to VDS and from VDS to applications.

</td>
</tr>
</table> 


## -remarks



VDS registers an <b>IVdsAdviseSink</b> interface with 
    providers by calling the 
    <a href="https://msdn.microsoft.com/c5b2ac78-6a23-470c-a762-26ce6358e0b6">IVdsProviderPrivate::OnLoad</a> method 
    implemented by the provider.

After implementing the <b>IVdsAdviseSink</b> 
      interface, an application must register the interface with VDS to receive notifications. To register, call the 
      <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>method and pass a pointer to the <b>IVdsAdviseSink</b> 
      interface. To unregister the <b>IVdsAdviseSink</b> interface and stop receiving notifications, use the <a href="https://msdn.microsoft.com/085d380c-2e09-470a-a23d-704c31535975">IVdsService::Unadvise</a> method.<div class="alert"><b>Note</b>  An application that calls <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">Advise</a> must eventually call <a href="https://msdn.microsoft.com/085d380c-2e09-470a-a23d-704c31535975">Unadvise</a>. Ideally, it should call <b>Unadvise</b> as soon as it no longer needs to receive notifications.</div>
<div> </div>


You do not specify a notification type or an object type when you register an application for notifications. 
     Rather, you register to receive all VDS notifications of all types and from all providers.




## -see-also




<a href="https://msdn.microsoft.com/c5b2ac78-6a23-470c-a762-26ce6358e0b6">IVdsProviderPrivate::OnLoad</a>



<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>



<a href="https://msdn.microsoft.com/a0841215-3eb0-4769-b320-4da25b535362">VDS Notifications</a>
 

 

