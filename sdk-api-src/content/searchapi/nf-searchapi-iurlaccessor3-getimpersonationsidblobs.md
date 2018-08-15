---
UID: NF:searchapi.IUrlAccessor3.GetImpersonationSidBlobs
title: IUrlAccessor3::GetImpersonationSidBlobs
author: windows-sdk-content
description: Retrieves an array of user security identifiers (SIDs) for a specified URL. This method enables protocol handlers to specify which users can access the file and the search protocol host to impersonate a user in order to index the file.
old-location: search\_search_IUrlAccessor3_GetImpersonationSidBlobs.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor3\getimpersonationsidblobs.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetImpersonationSidBlobs, GetImpersonationSidBlobs method [search], GetImpersonationSidBlobs method [search],IUrlAccessor3 interface, GetImpersonationSidBlobs method [search],IUrlAccessor4 interface, IUrlAccessor3 interface [search],GetImpersonationSidBlobs method, IUrlAccessor3.GetImpersonationSidBlobs, IUrlAccessor3::GetImpersonationSidBlobs, IUrlAccessor4 interface [search],GetImpersonationSidBlobs method, IUrlAccessor4::GetImpersonationSidBlobs, _search_IUrlAccessor3_GetImpersonationSidBlobs, search._search_IUrlAccessor3_GetImpersonationSidBlobs, searchapi/IUrlAccessor3::GetImpersonationSidBlobs, searchapi/IUrlAccessor4::GetImpersonationSidBlobs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.redist: Windows Search (WS) 4.0
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista with SP2 [desktop apps only]
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
 - IUrlAccessor3.GetImpersonationSidBlobs
 - IUrlAccessor4.GetImpersonationSidBlobs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IUrlAccessor3::GetImpersonationSidBlobs


## -description


Retrieves an array of user security identifiers (SIDs) for a specified URL. This method enables protocol handlers to specify which users can access the file and the search protocol host to impersonate a user in order to index the file.
        


## -parameters




### -param pcwszURL [in]

Type: <b>LPCWSTR</b>

The URL to access on behalf of an impersonated user.
                


### -param pcSidCount [out]

Type: <b>DWORD*</b>

Receives a pointer to the number of user SIDs returned in <i>ppSidBlobs</i>.
                


### -param ppSidBlobs [out]

Type: <b>BLOB**</b>

Receives the address of a pointer to the array of candidate impersonation user SIDs.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the file is encrypted, this method identifies who can both decrypt and access it. If the method cannot identify this information, it fails with error code E_ACCESSDENIED.
            

This method assumes that the <a href="https://msdn.microsoft.com/en-us/library/Bb231412(v=VS.85).aspx">IUrlAccessor2</a> object failed to initialize and returned the code <a href="https://msdn.microsoft.com/en-us/library/Aa965709(v=VS.85).aspx">PRTH_S_TRY_IMPERSONATING</a>. Then, the search protocol host calls this method to retrieve a list of SIDs to use for impersonation and reverts to using <b>IUrlAccessor2</b>, impersonating one of the allowed users when opening the item.

Impersonating a user does not elevate the caller's privileges. If the caller cannot directly retrieve the list of users authorized to access a resource, the caller won't be able to do that with this method, either. Only the search protocol host and the indexer have adequate privileges to impersonate users currently logged on.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Cc142931(v=VS.85).aspx">IUrlAccessor3</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd183431(v=VS.85).aspx">IUrlAccessor4</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965709(v=VS.85).aspx">Search Protocol Handler Error Messages</a>
 

 

