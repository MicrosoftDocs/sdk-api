---
UID: NF:shobjidl.IHWEventHandler.Initialize
title: IHWEventHandler::Initialize (shobjidl.h)
author: windows-sdk-content
description: Initializes an object that contains an implementation of the IHWEventHandler interface.
old-location: shell\IHWEventHandler_Initialize.htm
tech.root: shell
ms.assetid: 96eb582a-4f32-4e13-ad01-8b5ffabab582
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IHWEventHandler interface [Windows Shell],Initialize method, IHWEventHandler.Initialize, IHWEventHandler::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IHWEventHandler interface, inet_IHWEventHandler_Initialize, shell.IHWEventHandler_Initialize, shobjidl/IHWEventHandler::Initialize
ms.topic: method
f1_keywords: 
 - "shobjidl/IHWEventHandler.Initialize"
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shimgvw.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shimgvw.dll
api_name:
 - IHWEventHandler.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IHWEventHandler::Initialize


## -description


Initializes an object that contains an implementation of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-ihweventhandler">IHWEventHandler</a> interface.


## -parameters




### -param pszParams [in]

Type: <b>LPCWSTR</b>

A pointer to a string buffer that contains the string from the following registry value.
          


<pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>Explorer</b>
                  <b>AutoPlayHandlers</b>
                     <b>Handlers</b>
                        <i>HandlerName</i>
                           <b>InitCmdLine</b> = string</pre>



## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method receives the registry string stored in the InitCmdLine value under the
        
         <b>AutoPlayHandlers</b>\<b>Handlers</b>\<i>HandlerName</i>key. Applications that have registered with AutoPlay as event handlers place this string into the registry as part of the registration process.
      



