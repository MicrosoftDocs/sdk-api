---
UID: NF:combaseapi.CoRegisterSurrogate
title: CoRegisterSurrogate function (combaseapi.h)
description: Registers the surrogate process through its ISurrogate interface pointer.
helpviewer_keywords: ["CoRegisterSurrogate","CoRegisterSurrogate function [COM]","_com_CoRegisterSurrogate","com.coregistersurrogate","combaseapi/CoRegisterSurrogate"]
old-location: com\coregistersurrogate.htm
tech.root: com
ms.assetid: 4d1c6ca6-ab21-429c-9433-7c95d9e757b5
ms.date: 12/05/2018
ms.keywords: CoRegisterSurrogate, CoRegisterSurrogate function [COM], _com_CoRegisterSurrogate, com.coregistersurrogate, combaseapi/CoRegisterSurrogate
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoRegisterSurrogate
 - combaseapi/CoRegisterSurrogate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-ole32-l1-1-0.dll
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoRegisterSurrogate
---

# CoRegisterSurrogate function


## -description

Registers the surrogate process through its <a href="/windows/desktop/api/objidl/nn-objidl-isurrogate">ISurrogate</a> interface pointer.

## -parameters

### -param pSurrogate [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-isurrogate">ISurrogate</a> interface on the surrogate process to be registered.

## -returns

This function returns S_OK to indicate that the surrogate process was registered successfully.

## -remarks

The <b>CoRegisterSurrogate</b> function sets a global interface pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-isurrogate">ISurrogate</a> interface implemented on the surrogate process. This pointer is set in the ole32 DLL loaded in the surrogate process. COM uses this global pointer in ole32 to call the methods of <b>ISurrogate</b>. This function is usually called by the surrogate implementation when it is launched.



As of Windows Server 2003, if a COM object application is registered as a service, COM verifies the registration. COM makes sure the process ID of the service, in the service control manager (SCM), matches the process ID of the registering process. If not, COM fails the registration.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-isurrogate">ISurrogate</a>



<a href="/windows/desktop/com/writing-a-custom-surrogate">Writing a Custom Surrogate</a>