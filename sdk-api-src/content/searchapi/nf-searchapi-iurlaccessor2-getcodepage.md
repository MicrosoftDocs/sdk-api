---
UID: NF:searchapi.IUrlAccessor2.GetCodePage
title: IUrlAccessor2::GetCodePage
author: windows-sdk-content
description: Gets the code page for properties of the URL item.
old-location: search\_search_IUrlAccessor2_GetCodePage.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor2\getcodepage.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetCodePage, GetCodePage method [search], GetCodePage method [search],IUrlAccessor2 interface, GetCodePage method [search],IUrlAccessor4 interface, IUrlAccessor2 interface [search],GetCodePage method, IUrlAccessor2.GetCodePage, IUrlAccessor2::GetCodePage, IUrlAccessor4 interface [search],GetCodePage method, IUrlAccessor4::GetCodePage, _search_IUrlAccessor2_GetCodePage, search._search_IUrlAccessor2_GetCodePage, searchapi/IUrlAccessor2::GetCodePage, searchapi/IUrlAccessor4::GetCodePage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Urlaccsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	IUrlAccessor2.GetCodePage
-	IUrlAccessor4.GetCodePage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IUrlAccessor2::GetCodePage


## -description



            Gets the code page for properties of the URL item.
        


## -parameters




### -param wszCodePage [out]

Type: <b>WCHAR[]</b>


                    Receives the code page as a null-terminated Unicode string.
                


### -param dwSize [in]

Type: <b>DWORD</b>


                    Size of <i>wszCodePage</i> 
                    in <b>TCHAR</b><b>s</b>.             
                


### -param pdwLength [out]

Type: <b>DWORD*</b>


                Receives a pointer to the number of
                <b>TCHAR</b><b>s</b> written to
               <i>wszCodePage</i>, not including the terminating <b>NULL</b> character. 
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



