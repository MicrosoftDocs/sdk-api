---
UID: NF:searchapi.ISearchProtocol.CloseAccessor
title: ISearchProtocol::CloseAccessor
author: windows-sdk-content
description: Closes a previously created IUrlAccessor object.
old-location: search\_search_ISearchProtocol_CloseAccessor.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocol\closeaccessor.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: CloseAccessor, CloseAccessor method [search], CloseAccessor method [search],ISearchProtocol interface, ISearchProtocol interface [search],CloseAccessor method, ISearchProtocol.CloseAccessor, ISearchProtocol::CloseAccessor, _search_ISearchProtocol_CloseAccessor, search._search_ISearchProtocol_CloseAccessor, searchapi/ISearchProtocol::CloseAccessor
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
req.idl: Srchprth.idl
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
 - ISearchProtocol.CloseAccessor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISearchProtocol::CloseAccessor


## -description



        Closes a previously created <a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a> object. 
        


## -parameters




### -param pAccessor [in]

Type: <b><a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a>*</b>


                    Pointer to the <a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a> object that was used to process the current URL item. 
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




              The protocol host will release the <i>pAccessor</i> pointer passed to this method when this method returns. Use this method to release any resources associated with the <a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a> object, freeing it for reuse by the protocol handler.
            


              Accessors can be created and maintained in a pool, as resources to be used by protocol handlers when needed, and this might improve performance. If you are implementing a pool of <a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a> objects, use <a href="_com_IUnknown_AddRef">IUnknown::AddRef</a> to add an <b>IUrlAccessor</b> to your pool.
            



