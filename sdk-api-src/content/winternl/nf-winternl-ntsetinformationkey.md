---
UID: NF:winternl.NtSetInformationKey
title: NtSetInformationKey function (winternl.h)
description: Sets information for the specified registry key.
helpviewer_keywords: ["NtSetInformationKey","NtSetInformationKey function [Windows API]","base.ntsetinformationkey","winprog.ntsetinformationkey","winternl/NtSetInformationKey"]
old-location: winprog\ntsetinformationkey.htm
tech.root: winprog
ms.assetid: 74772ebf-684b-4579-a28a-9b80afb4ccf9
ms.date: 12/05/2018
ms.keywords: NtSetInformationKey, NtSetInformationKey function [Windows API], base.ntsetinformationkey, winprog.ntsetinformationkey, winternl/NtSetInformationKey
f1_keywords:
- winternl/NtSetInformationKey
dev_langs:
- c++
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: Ntdll.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ntdll.dll
api_name:
- NtSetInformationKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NtSetInformationKey function


## -description


<p class="CCE_Message">[This function may be changed or removed from Windows without further notice.]

Sets information for the specified registry key.


## -parameters




### -param KeyHandle [in]

A handle to the registry key. The handle must be opened with the <b>KEY_WRITE</b> access 
      right.


### -param KeySetInformationClass [in]

A <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/ne-wdm-_key_set_information_class">KEY_SET_INFORMATION_CLASS</a> value that 
      specifies the kind of information to be set.


### -param KeySetInformation [in]

A pointer to the buffer that contains the information to be set. The format of this buffer is determined by 
      the <i>KeySetInformationClass</i> parameter.


### -param KeySetInformationLength [in]

The length of the buffer specified by the <i>KeySetInformation</i> parameter, in 
      bytes.


## -returns



Returns an <b>NTSTATUS</b> or error code. An error code of 
       <b>STATUS_INFO_LENGTH_MISMATCH</b> indicates that the 
       <i>KeySetInformationLength</i> parameter is the wrong length for the information class 
       specified by the <i>KeySetInformationClass</i> parameter.

The forms and significance of <b>NTSTATUS</b> error codes are listed in the Ntstatus.h 
       header file available in the WDK, and are described in the WDK documentation.




## -remarks



The associated import library, Ntdll.lib, is available in the 
    WDK. You can also use the <a href="https://docs.microsoft.com/windows/desktop/DevNotes/-loadlibrary">LoadLibrary</a> and 
    <a href="https://docs.microsoft.com/windows/desktop/DevNotes/-getprocaddress-">GetProcAddress</a> functions to dynamically link to 
    Ntdll.dll.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>
 

 

