---
UID: NF:iads.IADsAccessControlList.RemoveAce
title: IADsAccessControlList::RemoveAce
author: windows-sdk-content
description: Removes an access-control entry (ACE) from the access-control list (ACL).
old-location: adsi\iadsaccesscontrollist_removeace.htm
old-project: ADSI
ms.assetid: 29c1ffcc-5a66-4ee3-889a-747953c604a4
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IADsAccessControlList interface [ADSI],RemoveAce method, IADsAccessControlList.RemoveAce, IADsAccessControlList::RemoveAce, RemoveAce, RemoveAce method [ADSI], RemoveAce method [ADSI],IADsAccessControlList interface, _ds_iadsaccesscontrollist_removeace, adsi.iadsaccesscontrollist__removeace, adsi.iadsaccesscontrollist_removeace, iads/IADsAccessControlList::RemoveAce
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: iads.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsAccessControlList.RemoveAce
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsAccessControlList::RemoveAce


## -description


The <b>IADsAccessControlList::RemoveAce</b> method removes an access-control entry (ACE) from the access-control list (ACL).


## -parameters




### -param pAccessControlEntry [in]

Pointer to the <b>IDispatch</b> interface of the ACE to be removed from the ACL.


## -returns



This method returns standard return values.

For more information, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/6d2cd45b-0dc6-4bb3-9c41-014bec71f258">IADsAccessControlEntry</a>



<a href="https://msdn.microsoft.com/de92d9cc-bc9d-4dc5-aa79-01f4d3050c35">IADsAccessControlList</a>



<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a>
 

 

