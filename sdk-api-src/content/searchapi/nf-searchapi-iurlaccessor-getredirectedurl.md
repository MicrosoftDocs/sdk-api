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

# IUrlAccessor::GetRedirectedURL


## -description



        Gets the redirected URL for the current item.
        


## -parameters




### -param wszRedirectedURL [out]

Type: <b>WCHAR[]</b>


                Receives the redirected URL as a Unicode string, not including the terminating <b>NULL</b>.
                


### -param dwSize [in]

Type: <b>DWORD</b>


                Size in <b>TCHAR</b><b>s</b>
                of <i>wszRedirectedURL</i>, not including the terminating <b>NULL</b>.
                


### -param pdwLength [out]

Type: <b>DWORD*</b>


                Receives a pointer to the number of
                <b>TCHAR</b><b>s</b> 
                written to <i>wszRedirectedURL</i>,
                not including the terminating <b>NULL</b>.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




             File URLs are not redirected. This method applies only to a content source of HTTP.
            


            If this method is implemented, the URL that is passed to <a href="https://msdn.microsoft.com/6fa8bf02-155d-48e9-8f94-c54680ae33e2">ISearchProtocol::CreateAccessor</a> will be redirected to the value returned by this method. All subsequent relative URL links will be processed based on the redirected URL.
            



