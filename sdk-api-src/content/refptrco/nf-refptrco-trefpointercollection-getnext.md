---
UID: NF:refptrco.TRefPointerCollection.GetNext
title: TRefPointerCollection::GetNext
author: windows-sdk-content
description: The GetNext method gets a pointer to the next instance in the collection.
old-location: wmi\trefpointercollection_getnext.htm
old-project: WmiSdk
ms.assetid: c0dfb2c7-71f6-4870-8018-145e890d4928
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: GetNext, GetNext method [Windows Management Instrumentation], GetNext method [Windows Management Instrumentation],TRefPointerCollection interface, TRefPointerCollection interface [Windows Management Instrumentation],GetNext method, TRefPointerCollection.GetNext, TRefPointerCollection::GetNext, _hmm_trefpointercollection_getnext, refptrco/TRefPointerCollection::GetNext, wmi.trefpointercollection_getnext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: refptrco.h
req.include-header: FwCommon.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RECO_RANGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - TRefPointerCollection.GetNext
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: ADAM
---

# TRefPointerCollection::GetNext


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/a2d1758a-4a7e-40fd-84c7-a25bc36ab538">TRefPointerCollection</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetNext</b> method gets a pointer to the next instance in the collection.


## -parameters




### -param pos [ref]

Denotes the position of an item in a <a href="https://msdn.microsoft.com/a2d1758a-4a7e-40fd-84c7-a25bc36ab538">TRefPointerCollection</a> collection.


## -returns



The <b>GetNext</b> method returns the address of the next item by position in the <a href="https://msdn.microsoft.com/a2d1758a-4a7e-40fd-84c7-a25bc36ab538">TRefPointerCollection</a> collection.



