---
UID: NS:winnt._PROCESS_MITIGATION_IMAGE_LOAD_POLICY
title: "_PROCESS_MITIGATION_IMAGE_LOAD_POLICY"
author: windows-sdk-content
description: Contains process mitigation policy settings for the loading of images from a remote device.
old-location: base\process_mitigation_image_load_policy.htm
tech.root: ProcThread
ms.assetid: C5B414D0-C209-4669-9E02-D7E453E242B1
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "*PPROCESS_MITIGATION_IMAGE_LOAD_POLICY, PPROCESS_MITIGATION_IMAGE_LOAD_POLICY, PPROCESS_MITIGATION_IMAGE_LOAD_POLICY structure pointer, PROCESS_MITIGATION_IMAGE_LOAD_POLICY, PROCESS_MITIGATION_IMAGE_LOAD_POLICY structure, _PROCESS_MITIGATION_IMAGE_LOAD_POLICY, base.process_mitigation_image_load_policy, winnt/PPROCESS_MITIGATION_IMAGE_LOAD_POLICY, winnt/PROCESS_MITIGATION_IMAGE_LOAD_POLICY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - WinNT.h
api_name:
 - PROCESS_MITIGATION_IMAGE_LOAD_POLICY
product: Windows
targetos: Windows
req.typenames: PROCESS_MITIGATION_IMAGE_LOAD_POLICY, *PPROCESS_MITIGATION_IMAGE_LOAD_POLICY
req.redist: 
---

# _PROCESS_MITIGATION_IMAGE_LOAD_POLICY structure


## -description


Contains process mitigation policy settings for the loading of images from a remote device.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Flags

Reserved for system use.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.NoRemoteImages

Set (0x1) to prevent the process from loading images from a remote device, such as a UNC share; otherwise leave unset (0x0).


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.NoLowMandatoryLabelImages

Set (0x1) to prevent the process from loading images that have a Low mandatory label, as written by low IL; otherwise leave unset (0x0).


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.PreferSystem32Images

Set (0x1) to search for images to load in the System32 subfolder of the folder in which Windows is installed first, then in the application directory in the standard DLL search order; otherwise leave unset (0x0).


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.AuditNoRemoteImages

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.AuditNoLowMandatoryLabelImages

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

Reserved for system use.


## -see-also




<a href="https://msdn.microsoft.com/89f9c883-6976-4af2-9a8b-c76101d8ed02">GetProcessMitigationPolicy</a>



<a href="https://msdn.microsoft.com/57f364f8-58d7-447a-91c3-51fc1fe1a481">SetProcessMitigationPolicy</a>
 

 

