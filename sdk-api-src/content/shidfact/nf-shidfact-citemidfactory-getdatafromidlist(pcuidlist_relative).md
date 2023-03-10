---
UID: NF:shidfact.CItemIDFactory.GetDataFromIDList(PCUIDLIST_RELATIVE)
title: CItemIDFactory::GetDataFromIDList(PCUIDLIST_RELATIVE) (shidfact.h)
description: Gets a read only pointer to the client provided structure in the first ItemID in the IDList. (overload 1/2)
helpviewer_keywords: ["CItemIDFactory interface [Windows Shell]","GetDataFromIDList method","CItemIDFactory.GetDataFromIDList","CItemIDFactory.GetDataFromIDList(PCUIDLIST_RELATIVE)","CItemIDFactory::GetDataFromIDList","CItemIDFactory::GetDataFromIDList(PCUIDLIST_RELATIVE)","GetDataFromIDList","GetDataFromIDList method [Windows Shell]","GetDataFromIDList method [Windows Shell]","CItemIDFactory interface","shell.citemidfactory_getdatafromidlist","shidfact/CItemIDFactory::GetDataFromIDList"]
old-location: shell\citemidfactory_getdatafromidlist.htm
tech.root: shell
ms.assetid: E3E2233D-F424-4BF9-AAC4-4DC2FB75E214
ms.date: 12/05/2018
ms.keywords: CItemIDFactory interface [Windows Shell],GetDataFromIDList method, CItemIDFactory.GetDataFromIDList, CItemIDFactory.GetDataFromIDList(PCUIDLIST_RELATIVE), CItemIDFactory::GetDataFromIDList, CItemIDFactory::GetDataFromIDList(PCUIDLIST_RELATIVE), GetDataFromIDList, GetDataFromIDList method [Windows Shell], GetDataFromIDList method [Windows Shell],CItemIDFactory interface, shell.citemidfactory_getdatafromidlist, shidfact/CItemIDFactory::GetDataFromIDList
req.header: shidfact.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CItemIDFactory::GetDataFromIDList
 - shidfact/CItemIDFactory::GetDataFromIDList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shidfact.h
api_name:
 - CItemIDFactory.GetDataFromIDList
---

# CItemIDFactory::GetDataFromIDList(PCUIDLIST_RELATIVE)


## -description

Gets a read only pointer to the client provided structure in the first ItemID in the IDList.

## -parameters

### -param pidl [in]

A PIDL containing the data.


#### - ppData [out]

When this method returns, contains the address of a read only pointer to a client provided structure.

## -returns

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns <b>E_INVALIDARG</b>.

## -see-also

<a href="/windows/desktop/api/shidfact/nl-shidfact-citemidfactory">CItemIDFactory</a>
