---
UID: NF:wuapi.IUpdateSearcher3.get_SearchScope
title: get_SearchScope function
author: windows-sdk-content
description: Gets and sets a SearchScope enumeration value which indicates the scope of the updates that are returned by the search.
old-location: wua\iupdatesearcher3_searchscope.htm
old-project: wua_sdk
ms.assetid: b01e3c3d-7f4d-445f-a08c-a7c1b20551b8
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUpdateSearcher3 interface [Windows Update Agent],SearchScope method, IUpdateSearcher3::SearchScope, SearchScope method [Windows Update Agent], SearchScope method [Windows Update Agent],IUpdateSearcher3 interface, get_SearchScope, put_SearchScope, wua.iupdatesearcher3_searchscope, wuapi/IUpdateSearcher3::SearchScope
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wuapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateSearcher3.SearchScope
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# get_SearchScope function


## -description



Gets and sets a <a href="https://msdn.microsoft.com/a7b6a930-7b79-42dc-a4b0-da2eca0dff5c">SearchScope</a> enumeration value which indicates the scope of the updates that are returned by the search.




## -parameters




### -param retval [out, retval]

A <a href="https://msdn.microsoft.com/a7b6a930-7b79-42dc-a4b0-da2eca0dff5c">SearchScope</a> value that specifies the scope of the search.


#### - value [in]

A <a href="https://msdn.microsoft.com/a7b6a930-7b79-42dc-a4b0-da2eca0dff5c">SearchScope</a> value that specifies the scope of the search.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d37017d5-6f78-4b6c-ac0b-c83b83853079">IUpdateSearcher3</a>
 

 

