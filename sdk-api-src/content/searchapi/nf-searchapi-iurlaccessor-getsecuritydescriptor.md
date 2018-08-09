---
UID: NF:searchapi.IUrlAccessor.GetSecurityDescriptor
title: IUrlAccessor::GetSecurityDescriptor
author: windows-sdk-content
description: Gets the security descriptor for the URL item. Security is applied at query time, so this descriptor identifies security for read access.
old-location: search\_search_IUrlAccessor_GetSecurityDescriptor.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\getsecuritydescriptor.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetSecurityDescriptor, GetSecurityDescriptor method [search], GetSecurityDescriptor method [search],IUrlAccessor interface, IUrlAccessor interface [search],GetSecurityDescriptor method, IUrlAccessor.GetSecurityDescriptor, IUrlAccessor::GetSecurityDescriptor, _search_IUrlAccessor_GetSecurityDescriptor, search._search_IUrlAccessor_GetSecurityDescriptor, searchapi/IUrlAccessor::GetSecurityDescriptor
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
 - IUrlAccessor.GetSecurityDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IUrlAccessor::GetSecurityDescriptor


## -description


Gets the security descriptor for the URL item. Security is applied at query time, so this descriptor identifies security for read access.
        


## -parameters




### -param pSD [out]

Type: <b>BYTE*</b>

Receives a pointer to the security descriptor.
                


### -param dwSize [in]

Type: <b>DWORD</b>

Size in <b>TCHAR</b><b>s</b>of the <i>pSD</i> array.
                


### -param pdwLength [out]

Type: <b>DWORD*</b>

Receives a pointer to the number of <b>TCHAR</b><b>s</b> written to <i>pSD</i>, not including the terminating <b>NULL</b>.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method allows custom mappings between users registered to a content source and those users registered on the domain, if they are different. Security descriptors created in this method must be self-relative.
            

If the URL contains a user security identifier (SID), then the protocol handler is invoked in the security context of that user, and this method must return E_NOTIMPL. 
            

If the URL does not contain a user SID, then the protocol handler is invoked in the security context of the system service. In that case, this method can return either an access control list (ACL) to restrict read access, or <a href="https://msdn.microsoft.com/en-us/library/Aa965709(v=VS.85).aspx">PRTH_S_ACL_IS_READ_EVERYONE</a> to allow anyone read access during querying.
            

<div class="alert"><b>Note</b>  If this method returns E_NOTIMPL and the URL does NOT contain a user SID, then the item is retrievable by all user queries.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb231426(v=VS.85).aspx">IUrlAccessor</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965709(v=VS.85).aspx">Search Protocol Handler Error Messages</a>
 

 

