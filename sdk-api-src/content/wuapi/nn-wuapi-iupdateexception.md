---
UID: NN:wuapi.IUpdateException
title: IUpdateException (wuapi.h)
description: Represents info about the aspects of search results returned in the ISearchResult object that were incomplete.
helpviewer_keywords: ["IUpdateException","IUpdateException interface [Windows Update Agent]","IUpdateException interface [Windows Update Agent]","described","wua.iupdateexception","wuapi/IUpdateException"]
old-location: wua\iupdateexception.htm
tech.root: wua
ms.assetid: 9e7458be-b411-4395-98f2-c92308f78371
ms.date: 12/05/2018
ms.keywords: IUpdateException, IUpdateException interface [Windows Update Agent], IUpdateException interface [Windows Update Agent],described, wua.iupdateexception, wuapi/IUpdateException
req.header: wuapi.h
req.include-header: 
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
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateException
 - wuapi/IUpdateException
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateException
---

# IUpdateException interface


## -description

Represents info about the aspects of search results returned in the <a href="/windows/desktop/api/wuapi/nn-wuapi-isearchresult">ISearchResult</a> object that were incomplete. For more info, see Remarks.

## -remarks

The <b>IUpdateException</b> object is returned as part of the <a href="/windows/desktop/api/wuapi/nf-wuapi-isearchresult-get_warnings">ISearchResult::Warnings</a> property when a search succeeds but can't return complete results. For example, Windows Update might not have been able to retrieve all of the update metadata for a given update from the server. In this situation, the search results returned in the <a href="/windows/desktop/api/wuapi/nn-wuapi-isearchresult">ISearchResult</a> object are usable, but they aren't necessarily complete. The properties of the <b>IUpdateException</b> objects that are returned by the <b>ISearchResult::Warnings</b> property contain info about the  aspects of the search that were incomplete. This info is unlikely to be useful programmatically, but can sometimes be useful for debugging.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>