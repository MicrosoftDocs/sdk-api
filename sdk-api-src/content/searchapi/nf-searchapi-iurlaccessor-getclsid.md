---
UID: NF:searchapi.IUrlAccessor.GetCLSID
title: IUrlAccessor::GetCLSID
author: windows-sdk-content
description: Gets the CLSID for the document type of the URL item being processed.
old-location: search\_search_IUrlAccessor_GetCLSID.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\getclsid.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCLSID, GetCLSID method [search], GetCLSID method [search],IUrlAccessor interface, IUrlAccessor interface [search],GetCLSID method, IUrlAccessor.GetCLSID, IUrlAccessor::GetCLSID, _search_IUrlAccessor_GetCLSID, search._search_IUrlAccessor_GetCLSID, searchapi/IUrlAccessor::GetCLSID
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
 - IUrlAccessor.GetCLSID
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IUrlAccessor::GetCLSID


## -description


Gets the <a href="https://msdn.microsoft.com/en-us/library/ms688628(v=VS.85).aspx">CLSID</a> for the document type of the URL item being processed.
        


## -parameters




### -param pClsid [out]

Type: <b>CLSID*</b>

Receives a pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms688628(v=VS.85).aspx">CLSID</a> for the document type of the URL item being processed. 
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If this information is not available, you can return E_NOTIMPL or E_FAIL.
            



