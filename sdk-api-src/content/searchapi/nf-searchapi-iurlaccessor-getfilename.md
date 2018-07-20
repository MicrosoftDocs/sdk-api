---
UID: NF:searchapi.IUrlAccessor.GetFileName
title: IUrlAccessor::GetFileName
author: windows-sdk-content
description: Retrieves the file name of the item, which the filter host uses for indexing. If the item does not exist in a file system and the IUrlAccessor::BindToStream method is implemented, this method returns the shell's System.ParsingPath property for the item.
old-location: search\_search_IUrlAccessor_GetFileName.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\getfilename.htm
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: GetFileName, GetFileName method [search], GetFileName method [search],IUrlAccessor interface, IUrlAccessor interface [search],GetFileName method, IUrlAccessor.GetFileName, IUrlAccessor::GetFileName, _search_IUrlAccessor_GetFileName, search._search_IUrlAccessor_GetFileName, searchapi/IUrlAccessor::GetFileName
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
 - IUrlAccessor.GetFileName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IUrlAccessor::GetFileName


## -description



        Retrieves the file name of the item, which the filter host uses for indexing. If the item does not exist in a file system and the <a href="https://msdn.microsoft.com/02dc13c0-01a4-416d-ba14-c0390b4c4aae">IUrlAccessor::BindToStream</a> method is implemented, this method returns the shell's System.ParsingPath property for the item. 
        


## -parameters




### -param wszFileName [out]

Type: <b>WCHAR[]</b>


                Receives the file name as a null-terminated Unicode string.
                


### -param dwSize [in]

Type: <b>DWORD</b>


                Size in 
                <b>TCHAR</b><b>s</b> of
                <i>wszFileName</i>, not including the terminating <b>NULL</b>.
                


### -param pdwLength [out]

Type: <b>DWORD*</b>


           Receives a pointer to the number of 
           <b>TCHAR</b><b>s</b>
            written to <b>wszFileName</b>, not including
                <b>NULL</b>.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




       If this method is implemented, the filter host uses the file name to determine the correct <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> to use to parse the content of the stream returned by <a href="https://msdn.microsoft.com/02dc13c0-01a4-416d-ba14-c0390b4c4aae">IUrlAccessor::BindToStream</a>. 
       
       



