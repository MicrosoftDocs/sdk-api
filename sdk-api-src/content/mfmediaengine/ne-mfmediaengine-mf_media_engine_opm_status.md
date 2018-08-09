---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_OPM_STATUS
title: MF_MEDIA_ENGINE_OPM_STATUS
author: windows-sdk-content
description: Defines the status of the Output Protection Manager (OPM).
old-location: mf\mf_media_engine_opm_status.htm
old-project: medfound
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MF_MEDIA_ENGINE_OPM_ESTABLISHED, MF_MEDIA_ENGINE_OPM_FAILED, MF_MEDIA_ENGINE_OPM_FAILED_BDA, MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER, MF_MEDIA_ENGINE_OPM_FAILED_VM, MF_MEDIA_ENGINE_OPM_NOT_REQUESTED, MF_MEDIA_ENGINE_OPM_STATUS, MF_MEDIA_ENGINE_OPM_STATUS enumeration [Media Foundation], mf.mf_media_engine_opm_status, mfmediaengine/MF_MEDIA_ENGINE_OPM_ESTABLISHED, mfmediaengine/MF_MEDIA_ENGINE_OPM_FAILED, mfmediaengine/MF_MEDIA_ENGINE_OPM_FAILED_BDA, mfmediaengine/MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER, mfmediaengine/MF_MEDIA_ENGINE_OPM_FAILED_VM, mfmediaengine/MF_MEDIA_ENGINE_OPM_NOT_REQUESTED, mfmediaengine/MF_MEDIA_ENGINE_OPM_STATUS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_MEDIA_ENGINE_OPM_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfmediaengine.h
api_name:
 - MF_MEDIA_ENGINE_OPM_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MF_MEDIA_ENGINE_OPM_STATUS enumeration


## -description


Defines the status of the <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>  (OPM).


## -enum-fields




### -field MF_MEDIA_ENGINE_OPM_NOT_REQUESTED

Default status. Used to return the correct status when the content is unprotected.


### -field MF_MEDIA_ENGINE_OPM_ESTABLISHED

OPM successfully established.


### -field MF_MEDIA_ENGINE_OPM_FAILED_VM

OPM failed because running in a virtual machined (VM).


### -field MF_MEDIA_ENGINE_OPM_FAILED_BDA

OPM failed because there is no graphics driver and the system is using Basic Display Adapter (BDA).


### -field MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER

OPM failed because the graphics 
driver is not PE signed, falling back to WARP.


### -field MF_MEDIA_ENGINE_OPM_FAILED

OPM failed for other reasons.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

