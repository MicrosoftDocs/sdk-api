---
UID: NF:wdstptmgmt.IWdsTransportNamespace.get_TombstoneTime
title: IWdsTransportNamespace::get_TombstoneTime
author: windows-sdk-content
description: Returns the UTC date and time when the server saved the namespace object of a deregistered namespace.
old-location: wds\iwdstransportnamespace_tombstonetime.htm
tech.root: wds
ms.assetid: 95516e2b-40e3-4da8-9ca0-0f96a8e6cb13
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IWdsTransportNamespace interface [Windows Deployment Services],TombstoneTime property, IWdsTransportNamespace.TombstoneTime, IWdsTransportNamespace.get_TombstoneTime, IWdsTransportNamespace::TombstoneTime, IWdsTransportNamespace::get_TombstoneTime, TombstoneTime property [Windows Deployment Services], TombstoneTime property [Windows Deployment Services],IWdsTransportNamespace interface, get_TombstoneTime, wds.iwdstransportnamespace_tombstonetime, wdstptmgmt/IWdsTransportNamespace::TombstoneTime, wdstptmgmt/IWdsTransportNamespace::get_TombstoneTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wdstptmgmt.tlb
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportNamespace.TombstoneTime
 - IWdsTransportNamespace.get_TombstoneTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wdstptmgmt.h
: 
- IWdsTransportNamespace.get_TombstoneTime
: 
---

# IWdsTransportNamespace::get_TombstoneTime


## -description


Returns the UTC date and time when the server saved the namespace object of a deregistered namespace.

This property is read-only.


## -parameters


## -remarks



If the namespace has not been deregistered, this property fails with an error that indicates that the namespace is not valid at this time.




## -see-also




<a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a>



<a href="https://msdn.microsoft.com/a04b578b-ad18-46b0-a60e-77647fa67aaf">Tombstoned Property</a>
 

 

