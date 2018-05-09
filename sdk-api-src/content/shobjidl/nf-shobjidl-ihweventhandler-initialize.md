---
UID: NF:shobjidl.IHWEventHandler.Initialize
title: IHWEventHandler::Initialize
author: windows-driver-content
description: Initializes an object that contains an implementation of the IHWEventHandler interface.
old-location: shell\IHWEventHandler_Initialize.htm
old-project: shell
ms.assetid: 96eb582a-4f32-4e13-ad01-8b5ffabab582
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: IHWEventHandler interface [Windows Shell],Initialize method, IHWEventHandler.Initialize, IHWEventHandler::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IHWEventHandler interface, inet_IHWEventHandler_Initialize, shell.IHWEventHandler_Initialize, shobjidl/IHWEventHandler::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shimgvw.dll
api_name:
-	IHWEventHandler.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: Shimgvw.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IHWEventHandler::Initialize


## -description


Initializes an object that contains an implementation of the <a href="https://msdn.microsoft.com/be49322a-99b2-4626-8e9d-29965bbe182d">IHWEventHandler</a> interface.


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
        
         <b>AutoPlayHandlers</b>\<b>Handlers</b>\<i>HandlerName</i>
        key. Applications that have registered with AutoPlay as event handlers place this string into the registry as part of the registration process.
      



