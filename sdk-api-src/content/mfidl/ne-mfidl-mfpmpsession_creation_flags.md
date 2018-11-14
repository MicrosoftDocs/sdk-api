---
UID: NE:mfidl.MFPMPSESSION_CREATION_FLAGS
title: MFPMPSESSION_CREATION_FLAGS
author: windows-sdk-content
description: Contains flags that define the behavior of the MFCreatePMPMediaSession function.
old-location: mf\mfpmpsession_creation_flags.htm
tech.root: medfound
ms.assetid: 6341aaff-aa80-4172-8577-0b757a01ea53
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 6341aaff-aa80-4172-8577-0b757a01ea53, MFPMPSESSION_CREATION_FLAGS, MFPMPSESSION_CREATION_FLAGS enumeration [Media Foundation], MFPMPSESSION_UNPROTECTED_PROCESS, mf.mfpmpsession_creation_flags, mfidl/MFPMPSESSION_CREATION_FLAGS, mfidl/MFPMPSESSION_UNPROTECTED_PROCESS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFPMPSESSION_CREATION_FLAGS
product: Windows
targetos: Windows
req.typenames: MFPMPSESSION_CREATION_FLAGS
req.redist: 
---

# MFPMPSESSION_CREATION_FLAGS enumeration


## -description


Contains flags that define the behavior of the <a href="https://msdn.microsoft.com/cb492e68-3d8a-49b2-8c0b-bee8065b53a8">MFCreatePMPMediaSession</a> function.
        


## -enum-fields




### -field MFPMPSESSION_UNPROTECTED_PROCESS

If this flag is set, the Protected Media Path (PMP) Media Session is created in an unprotected process. You can use the unprotected process to play clear content but not protected content. If this flag is not set, the PMP Media Session is created in a protected process. In that case, the protected process is used for both protected content and clear content.


### -field MFPMPSESSION_IN_PROCESS




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

