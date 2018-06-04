---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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


<pre xml:space="preserve"><b>HKLM</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>Explorer</b>
                  <b>AutoplayHandlers</b>
                     <b>Handlers</b>
                        <b>YourHandler</b>
                           <b>DynamicHWHandlerCLSID</b> = [REG_SZ] {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</pre>




