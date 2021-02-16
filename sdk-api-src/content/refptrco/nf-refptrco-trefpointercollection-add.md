---
UID: NF:refptrco.TRefPointerCollection.Add
title: TRefPointerCollection::Add (refptrco.h)
description: The Add method adds a reference to the collection.
helpviewer_keywords: ["Add","Add method [Windows Management Instrumentation]","Add method [Windows Management Instrumentation]","TRefPointerCollection interface","TRefPointerCollection interface [Windows Management Instrumentation]","Add method","TRefPointerCollection.Add","TRefPointerCollection::Add","_hmm_trefpointercollection_add","refptrco/TRefPointerCollection::Add","wmi.trefpointercollection_add"]
old-location: wmi\trefpointercollection_add.htm
tech.root: wmi
ms.assetid: 959cd8e7-ea0c-4b98-8e13-398e09c62668
ms.date: 12/05/2018
ms.keywords: Add, Add method [Windows Management Instrumentation], Add method [Windows Management Instrumentation],TRefPointerCollection interface, TRefPointerCollection interface [Windows Management Instrumentation],Add method, TRefPointerCollection.Add, TRefPointerCollection::Add, _hmm_trefpointercollection_add, refptrco/TRefPointerCollection::Add, wmi.trefpointercollection_add
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TRefPointerCollection::Add
 - refptrco/TRefPointerCollection::Add
dev_langs:
 - c++
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
---

# TRefPointerCollection::Add


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/refptrco/nl-refptrco-trefpointercollection">TRefPointerCollection</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Add</b> method adds a reference to the collection.

## -parameters

### -param ptr

Pointer to be added to the collection.

## -returns

If the method is successful, it returns <b>TRUE</b>.

If the method fails, it returns <b>FALSE</b>.

## -remarks

The <b>Add</b> method calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on this pointer.