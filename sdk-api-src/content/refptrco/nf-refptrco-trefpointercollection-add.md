---
UID: NF:refptrco.TRefPointerCollection.Add
title: TRefPointerCollection::Add
author: windows-sdk-content
description: The Add method adds a reference to the collection.
old-location: wmi\trefpointercollection_add.htm
tech.root: WmiSdk
ms.assetid: 959cd8e7-ea0c-4b98-8e13-398e09c62668
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Add, Add method [Windows Management Instrumentation], Add method [Windows Management Instrumentation],TRefPointerCollection interface, TRefPointerCollection interface [Windows Management Instrumentation],Add method, TRefPointerCollection.Add, TRefPointerCollection::Add, _hmm_trefpointercollection_add, refptrco/TRefPointerCollection::Add, wmi.trefpointercollection_add
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: refptrco.h
req.include-header: FwCommon.h
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
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - TRefPointerCollection.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TRefPointerCollection::Add


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/a2d1758a-4a7e-40fd-84c7-a25bc36ab538">TRefPointerCollection</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>Add</b> method adds a reference to the collection.


## -parameters




### -param ptr

Pointer to be added to the collection.


## -returns



If the method is successful, it returns <b>TRUE</b>.

If the method fails, it returns <b>FALSE</b>.




## -remarks



The <b>Add</b> method calls the <a href="_com_iunknown_addref">AddRef</a> method on this pointer.



