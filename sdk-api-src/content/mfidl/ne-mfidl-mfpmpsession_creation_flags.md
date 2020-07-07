---
UID: NE:mfidl.MFPMPSESSION_CREATION_FLAGS
title: MFPMPSESSION_CREATION_FLAGS (mfidl.h)
description: Contains flags that define the behavior of the MFCreatePMPMediaSession function.
helpviewer_keywords: ["6341aaff-aa80-4172-8577-0b757a01ea53","MFPMPSESSION_CREATION_FLAGS","MFPMPSESSION_CREATION_FLAGS enumeration [Media Foundation]","MFPMPSESSION_UNPROTECTED_PROCESS","mf.mfpmpsession_creation_flags","mfidl/MFPMPSESSION_CREATION_FLAGS","mfidl/MFPMPSESSION_UNPROTECTED_PROCESS"]
old-location: mf\mfpmpsession_creation_flags.htm
tech.root: medfound
ms.assetid: 6341aaff-aa80-4172-8577-0b757a01ea53
ms.date: 12/05/2018
ms.keywords: 6341aaff-aa80-4172-8577-0b757a01ea53, MFPMPSESSION_CREATION_FLAGS, MFPMPSESSION_CREATION_FLAGS enumeration [Media Foundation], MFPMPSESSION_UNPROTECTED_PROCESS, mf.mfpmpsession_creation_flags, mfidl/MFPMPSESSION_CREATION_FLAGS, mfidl/MFPMPSESSION_UNPROTECTED_PROCESS
f1_keywords:
- mfidl/MFPMPSESSION_CREATION_FLAGS
dev_langs:
- c++
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
targetos: Windows
req.typenames: MFPMPSESSION_CREATION_FLAGS
req.redist: 
ms.custom: 19H1
---

# MFPMPSESSION_CREATION_FLAGS enumeration


## -description


Contains flags that define the behavior of the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession">MFCreatePMPMediaSession</a> function.
        


## -enum-fields




### -field MFPMPSESSION_UNPROTECTED_PROCESS

If this flag is set, the Protected Media Path (PMP) Media Session is created in an unprotected process. You can use the unprotected process to play clear content but not protected content. If this flag is not set, the PMP Media Session is created in a protected process. In that case, the protected process is used for both protected content and clear content.


### -field MFPMPSESSION_IN_PROCESS




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
 

 

