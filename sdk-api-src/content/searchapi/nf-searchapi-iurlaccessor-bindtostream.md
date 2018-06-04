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

# IUrlAccessor::BindToStream


## -description



        Binds the item being processed to an <a href="_stg_istream">IStream interface [Structured Storage]</a> data stream and retrieves a pointer to that stream.
        


## -parameters




### -param ppStream [out]

Type: <b>IStream**</b>


                Receives the address of a pointer to the <a href="_stg_istream">IStream</a> that contains the item represented by the URL.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 Using the information returned by the <a href="https://msdn.microsoft.com/410be931-d458-458a-b0cd-4e9f0c444423">IUrlAccessor::GetFileName</a>, <a href="https://msdn.microsoft.com/dc56bacc-17a9-450f-a57c-22a90bde24b8">IUrlAccessor::GetCLSID</a>, and <a href="https://msdn.microsoft.com/2847de4b-79bb-4596-a0ed-fd494046aab4">IUrlAccessor::GetDocFormat</a> methods, the appropriate content <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>object is created and passed to this stream by the IPersistStream interface.
            



