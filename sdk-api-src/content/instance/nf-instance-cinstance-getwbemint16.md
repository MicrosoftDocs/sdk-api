---
UID: NF:instance.CInstance.GetWBEMINT16
title: CInstance::GetWBEMINT16 (instance.h)
description: The GetWBEMINT16 method retrieves a 16-bit integer property.
helpviewer_keywords: ["?GetWBEMINT16@CInstance@@QBE_NPBGAAF@Z","?GetWBEMINT16@CInstance@@QEBA_NPEBGAEAF@Z","CInstance interface [Windows Management Instrumentation]","GetWBEMINT16 method","CInstance.GetWBEMINT16","CInstance::GetWBEMINT16","GetWBEMINT16","GetWBEMINT16 method [Windows Management Instrumentation]","GetWBEMINT16 method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_getwbemint16","instance/CInstance::GetWBEMINT16","wmi.cinstance_getwbemint16"]
old-location: wmi\cinstance_getwbemint16.htm
tech.root: wmi
ms.assetid: 9f22a939-58a9-4444-8d17-04330cded7d1
ms.date: 12/05/2018
ms.keywords: ?GetWBEMINT16@CInstance@@QBE_NPBGAAF@Z, ?GetWBEMINT16@CInstance@@QEBA_NPEBGAEAF@Z, CInstance interface [Windows Management Instrumentation],GetWBEMINT16 method, CInstance.GetWBEMINT16, CInstance::GetWBEMINT16, GetWBEMINT16, GetWBEMINT16 method [Windows Management Instrumentation], GetWBEMINT16 method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getwbemint16, instance/CInstance::GetWBEMINT16, wmi.cinstance_getwbemint16
req.header: instance.h
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
 - CInstance::GetWBEMINT16
 - instance/CInstance::GetWBEMINT16
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CInstance.GetWBEMINT16
 - ?GetWBEMINT16@CInstance@@QBE_NPBGAAF@Z
 - ?GetWBEMINT16@CInstance@@QEBA_NPEBGAEAF@Z
---

# CInstance::GetWBEMINT16


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetWBEMINT16</b> method retrieves a 16-bit integer property.

## -parameters

### -param name

Name of the 16-bit integer property retrieved.

### -param wbemint16 [ref]

Buffer to receive the 16-bit integer property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to retrieve a nonexistent property or a property that was not a 16-bit integer. More information is available in the log file, Framework.log.