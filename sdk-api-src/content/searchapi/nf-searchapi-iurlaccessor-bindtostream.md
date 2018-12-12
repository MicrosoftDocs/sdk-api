---
UID: NF:searchapi.IUrlAccessor.BindToStream
title: IUrlAccessor::BindToStream
author: windows-sdk-content
description: Binds the item being processed to an IStream interface [Structured Storage] data stream and retrieves a pointer to that stream.
old-location: search\_search_IUrlAccessor_BindToStream.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\bindtostream.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BindToStream, BindToStream method [search], BindToStream method [search],IUrlAccessor interface, IUrlAccessor interface [search],BindToStream method, IUrlAccessor.BindToStream, IUrlAccessor::BindToStream, _search_IUrlAccessor_BindToStream, search._search_IUrlAccessor_BindToStream, searchapi/IUrlAccessor::BindToStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Urlaccsdk.idl
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
 - Searchapi.h
api_name:
 - IUrlAccessor.BindToStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
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
            



