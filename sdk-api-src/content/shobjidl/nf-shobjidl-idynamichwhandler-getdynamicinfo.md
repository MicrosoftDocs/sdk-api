---
UID: NF:shobjidl.IDynamicHWHandler.GetDynamicInfo
title: IDynamicHWHandler::GetDynamicInfo (shobjidl.h)
description: Called by the system to determine whether a particular handler will be shown before the AutoPlay dialog is displayed.
helpviewer_keywords: ["GetDynamicInfo","GetDynamicInfo method [Windows Shell]","GetDynamicInfo method [Windows Shell]","IDynamicHWHandler interface","IDynamicHWHandler interface [Windows Shell]","GetDynamicInfo method","IDynamicHWHandler.GetDynamicInfo","IDynamicHWHandler::GetDynamicInfo","_shell_IDynamicHWHandler_GetDynamicInfo","shell.IDynamicHWHandler_GetDynamicInfo","shobjidl/IDynamicHWHandler::GetDynamicInfo"]
old-location: shell\IDynamicHWHandler_GetDynamicInfo.htm
tech.root: shell
ms.assetid: 4477600b-311e-4425-b1de-9ed9c396fbdb
ms.date: 12/05/2018
ms.keywords: GetDynamicInfo, GetDynamicInfo method [Windows Shell], GetDynamicInfo method [Windows Shell],IDynamicHWHandler interface, IDynamicHWHandler interface [Windows Shell],GetDynamicInfo method, IDynamicHWHandler.GetDynamicInfo, IDynamicHWHandler::GetDynamicInfo, _shell_IDynamicHWHandler_GetDynamicInfo, shell.IDynamicHWHandler_GetDynamicInfo, shobjidl/IDynamicHWHandler::GetDynamicInfo
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDynamicHWHandler::GetDynamicInfo
 - shobjidl/IDynamicHWHandler::GetDynamicInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IDynamicHWHandler.GetDynamicInfo
---

# IDynamicHWHandler::GetDynamicInfo


## -description

Called by the system to determine whether a particular handler will be shown before the AutoPlay dialog is displayed.

## -parameters

### -param pszDeviceID [in]

Type: <b>LPCWSTR</b>

A pointer to a string that indicates the device path or drive root.

### -param dwContentType [in]

Type: <b>DWORD</b>

The content type.

### -param ppszAction [out]

Type: <b>LPWSTR*</b>

A pointer to the new action string, or <b>NULL</b> if the default action string is to be used.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if this handler is to be displayed, S_FALSE if it is to be hidden, or an error value otherwise.

## -remarks

To register a dynamic handler, add a REG_SZ named "DynamicHWHandlerCLSID" and assign it the CLSID of your IDynamicHWHandler implementation.

Example:


<pre><b>HKLM</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>Explorer</b>
                  <b>AutoplayHandlers</b>
                     <b>Handlers</b>
                        <b>YourHandler</b>
                           <b>DynamicHWHandlerCLSID</b> = [REG_SZ] {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</pre>

