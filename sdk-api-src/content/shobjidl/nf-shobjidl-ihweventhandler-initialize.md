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
      



