---
UID: NF:searchapi.IUrlAccessor.GetCLSID
title: IUrlAccessor::GetCLSID
author: windows-sdk-content
description: Gets the CLSID for the document type of the URL item being processed.
old-location: search\_search_IUrlAccessor_GetCLSID.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\getclsid.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: GetCLSID, GetCLSID method [search], GetCLSID method [search],IUrlAccessor interface, IUrlAccessor interface [search],GetCLSID method, IUrlAccessor.GetCLSID, IUrlAccessor::GetCLSID, _search_IUrlAccessor_GetCLSID, search._search_IUrlAccessor_GetCLSID, searchapi/IUrlAccessor::GetCLSID
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ROWSETEVENT_TYPE
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
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IUrlAccessor::GetCLSID


## -description



        Gets the <a href="_com_CLSID_Key">CLSID</a> for the document type of the URL item being processed.
        


## -parameters




### -param pClsid [out]

Type: <b>CLSID*</b>


                    Receives a pointer to the <a href="_com_CLSID_Key">CLSID</a> for the document type of the URL item being processed. 
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




                If this information is not available, you can return E_NOTIMPL or E_FAIL.
            



