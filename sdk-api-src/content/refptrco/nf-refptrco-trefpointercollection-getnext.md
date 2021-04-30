---
UID: NF:refptrco.TRefPointerCollection.GetNext
title: TRefPointerCollection::GetNext (refptrco.h)
description: The GetNext method gets a pointer to the next instance in the collection.
helpviewer_keywords: ["GetNext","GetNext method [Windows Management Instrumentation]","GetNext method [Windows Management Instrumentation]","TRefPointerCollection interface","TRefPointerCollection interface [Windows Management Instrumentation]","GetNext method","TRefPointerCollection.GetNext","TRefPointerCollection::GetNext","_hmm_trefpointercollection_getnext","refptrco/TRefPointerCollection::GetNext","wmi.trefpointercollection_getnext"]
old-location: wmi\trefpointercollection_getnext.htm
tech.root: wmi
ms.assetid: c0dfb2c7-71f6-4870-8018-145e890d4928
ms.date: 12/05/2018
ms.keywords: GetNext, GetNext method [Windows Management Instrumentation], GetNext method [Windows Management Instrumentation],TRefPointerCollection interface, TRefPointerCollection interface [Windows Management Instrumentation],GetNext method, TRefPointerCollection.GetNext, TRefPointerCollection::GetNext, _hmm_trefpointercollection_getnext, refptrco/TRefPointerCollection::GetNext, wmi.trefpointercollection_getnext
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
 - TRefPointerCollection::GetNext
 - refptrco/TRefPointerCollection::GetNext
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
 - TRefPointerCollection.GetNext
---

# TRefPointerCollection::GetNext


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/refptrco/nl-refptrco-trefpointercollection">TRefPointerCollection</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetNext</b> method gets a pointer to the next instance in the collection.

## -parameters

### -param pos [ref]

Denotes the position of an item in a <a href="/windows/desktop/api/refptrco/nl-refptrco-trefpointercollection">TRefPointerCollection</a> collection.

## -returns

The <b>GetNext</b> method returns the address of the next item by position in the <a href="/windows/desktop/api/refptrco/nl-refptrco-trefpointercollection">TRefPointerCollection</a> collection.