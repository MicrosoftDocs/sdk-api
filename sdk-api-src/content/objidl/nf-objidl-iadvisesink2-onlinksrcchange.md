---
UID: NF:objidl.IAdviseSink2.OnLinkSrcChange
title: IAdviseSink2::OnLinkSrcChange
author: windows-sdk-content
description: Notifies the container that registered the advise sink that a link source has changed (either name or location), enabling the container to update the link's moniker.
old-location: com\iadvisesink2_onlinksrcchange.htm
old-project: com
ms.assetid: 753ac9a3-0207-4c98-9d86-5ac16be2c5fa
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAdviseSink2 interface [COM],OnLinkSrcChange method, IAdviseSink2.OnLinkSrcChange, IAdviseSink2::OnLinkSrcChange, OnLinkSrcChange, OnLinkSrcChange method [COM], OnLinkSrcChange method [COM],IAdviseSink2 interface, _ole_iadvisesink2_onlinksrcchange, com.iadvisesink2_onlinksrcchange, objidl/IAdviseSink2::OnLinkSrcChange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IAdviseSink2.OnLinkSrcChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IAdviseSink2::OnLinkSrcChange


## -description


Notifies the container that registered the advise sink that a link source has changed (either name or location), enabling the container to update the link's moniker.


## -parameters




### -param pmk [in]

A pointer to the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface identifying the source of a linked object.


## -returns



This method does not return a value.




## -remarks



A container of linked objects implements this method to receive notification in the event of a change in the moniker of its link source.

<b>OnLinkSrcChange</b> is called by the OLE link object when it receives the <a href="https://msdn.microsoft.com/ec9926fb-d69e-430c-b67d-24c52d806bb5">OnRename</a> notification from the link-source (object) application. The link object updates its moniker and sends the <b>OnLinkSrcChange</b> notification to containers that have implemented <a href="https://msdn.microsoft.com/80f55377-8a1e-42b1-8fe0-5896620c8062">IAdviseSink2</a>.


<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Nothing prevents a link object from notifying its container of the moniker change by calling <a href="https://msdn.microsoft.com/ec9926fb-d69e-430c-b67d-24c52d806bb5">OnRename</a> instead of <b>OnLinkSrcChange</b>. In practice, however, overloading <b>OnRename</b> to mean either that a link object's moniker has changed or that an embedded object's server name has changed makes it difficult for applications to determine which of these events has occurred. If the two events trigger different processing, as will often be the case, calling a different method for each makes the job of determining which event occurred much easier.




## -see-also




<a href="https://msdn.microsoft.com/80f55377-8a1e-42b1-8fe0-5896620c8062">IAdviseSink2</a>



<a href="https://msdn.microsoft.com/ec9926fb-d69e-430c-b67d-24c52d806bb5">IAdviseSink::OnRename</a>
 

 

