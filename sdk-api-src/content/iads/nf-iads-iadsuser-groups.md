---
UID: NF:iads.IADsUser.Groups
title: IADsUser::Groups
author: windows-sdk-content
description: Obtains a collection of the ADSI group objects to which this user belongs.
old-location: adsi\iadsuser_groups.htm
tech.root: ADSI
ms.assetid: 0d250815-a7d8-4e61-b125-a66f1c2fde43
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Groups, Groups method [ADSI], Groups method [ADSI],IADsUser interface, IADsUser interface [ADSI],Groups method, IADsUser.Groups, IADsUser::Groups, _ds_iadsuser_groups, adsi.iadsuser__groups, adsi.iadsuser_groups, iads/IADsUser::Groups
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: iads.h
req.include-header: 
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
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsUser.Groups
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- iads.h
: 
- IADsUser.Groups
: 
---

# IADsUser::Groups


## -description


The <b>IADsUser::Groups</b> method obtains a collection of the ADSI group objects to which this user belongs. The method returns an  <a href="https://msdn.microsoft.com/889e8fc1-61a6-4a3a-82ac-85d41f664149">IADsMembers</a> interface pointer through which you can enumerate all the groups in the collection.


## -parameters




### -param ppGroups [out]

Pointer to a pointer to the <a href="https://msdn.microsoft.com/889e8fc1-61a6-4a3a-82ac-85d41f664149">IADsMembers</a> interface on a members object that can be enumerated using  <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> to determine the groups to which this end-user belongs.


## -returns



This method supports the standard return values, including S_OK. For other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/889e8fc1-61a6-4a3a-82ac-85d41f664149">IADsMembers</a>



<a href="https://msdn.microsoft.com/6eea74c2-2d6d-4dfd-9a22-3da2d5ce49bf">IADsUser</a>



<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">IADsUser
  Property Methods</a>



<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>
 

 

