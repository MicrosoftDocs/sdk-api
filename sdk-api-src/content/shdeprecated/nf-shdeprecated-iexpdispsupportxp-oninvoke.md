---
UID: NF:shdeprecated.IExpDispSupportXP.OnInvoke
title: IExpDispSupportXP::OnInvoke
author: windows-sdk-content
description: Not implemented.
old-location: shell\IExpDispSupportXP_OnInvoke.htm
tech.root: shell
ms.assetid: 92ae2e5c-466e-4f73-a2e3-7d040e756a50
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IExpDispSupportXP interface [Windows Shell],OnInvoke method, IExpDispSupportXP.OnInvoke, IExpDispSupportXP::OnInvoke, OnInvoke, OnInvoke method [Windows Shell], OnInvoke method [Windows Shell],IExpDispSupportXP interface, _shell_IExpDispSupportXP_OnInvoke, shdeprecated/IExpDispSupportXP::OnInvoke, shell.IExpDispSupportXP_OnInvoke
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shdeprecated.h
req.include-header: Shdeprecated.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
 - COM
api_location:
 - shdeprecated.h
api_name:
 - IExpDispSupportXP.OnInvoke
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExpDispSupportXP::OnInvoke


## -description


Not implemented.


## -parameters




### -param dispidMember

Type: <b>DISPID</b>

Specifies a dispatch ID that identifies the member being invoked.


### -param iid

Type: <b>REFIID</b>

Reserved. Must be IID_NULL.


### -param lcid

Type: <b>LCID</b>

Specifies a locale ID providing a locale context in which to interpret arguments. Applications that do not support multiple national languages can ignore this parameter.


### -param wFlags

Type: <b>WORD</b>

Specifies flags describing the context of the call.


### -param pdispparams [in]

Type: <b><a href="a16e5a21-766e-4287-b039-13429aa78f8b">DISPPARAMS</a>*</b>

Specifies a pointer to a <a href="a16e5a21-766e-4287-b039-13429aa78f8b">DISPPARAMS</a> structure containing an array of arguments, an array of argument DISPIDs for named arguments, and counts for the number of elements in the arrays.


### -param pVarResult [out]

Type: <b>VARIANT*</b>

Receives a pointer to the location where the result is to be stored, or <b>NULL</b> if the calling application expects no result. This argument is ignored if DISPATCH_PROPERTYPUT or DISPATCH_PROPERTYPUTREF is specified.


### -param pexcepinfo [out]

Type: <b>EXCEPINFO*</b>

Receives a pointer to a structure that contains exception information. This structure should be filled in if DISP_E_EXCEPTION is returned. Can be <b>NULL</b>.


### -param puArgErr [out]

Type: <b>UINT*</b>

Receives the index within the <b>rgvarg</b> member of the <a href="a16e5a21-766e-4287-b039-13429aa78f8b">DISPPARAMS</a> structure of the first argument that has an error.


## -returns



Type: <b>HRESULT</b>

Returns E_NOTIMPL.



