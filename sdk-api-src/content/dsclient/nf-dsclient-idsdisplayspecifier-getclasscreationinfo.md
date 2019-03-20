---
UID: NF:dsclient.IDsDisplaySpecifier.GetClassCreationInfo
title: IDsDisplaySpecifier::GetClassCreationInfo (dsclient.h)
author: windows-sdk-content
description: Retrieves data about the class creation wizard objects for a given object class.
old-location: ad\idsdisplayspecifier_getclasscreationinfo.htm
tech.root: ad
ms.assetid: 23b88707-c4c3-47dd-a5bc-e325142602f5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetClassCreationInfo, GetClassCreationInfo method [Active Directory], GetClassCreationInfo method [Active Directory],IDsDisplaySpecifier interface, IDsDisplaySpecifier interface [Active Directory],GetClassCreationInfo method, IDsDisplaySpecifier.GetClassCreationInfo, IDsDisplaySpecifier::GetClassCreationInfo, _glines_idsdisplayspecifier_getclasscreationinfo, ad.idsdisplayspecifier__getclasscreationinfo, ad.idsdisplayspecifier_getclasscreationinfo, dsclient/IDsDisplaySpecifier::GetClassCreationInfo
ms.topic: method
req.header: dsclient.h
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
req.dll: Dsadmin.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsadmin.dll
api_name:
 - IDsDisplaySpecifier.GetClassCreationInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsDisplaySpecifier::GetClassCreationInfo


## -description


The <b>IDsDisplaySpecifier::GetClassCreationInfo</b> method retrieves data about the class creation wizard objects for a given object class.


## -parameters




### -param pszObjectClass [in]

Pointer to a null-terminated Unicode string that contains the name of the attribute to obtain the <b>ADsType</b>  for.


### -param ppdscci [in]

Pointer to a <a href="https://msdn.microsoft.com/5c1551f7-f651-4b87-829a-ec9a07fb0ec2">DSCLASSCREATIONINFO</a> structure pointer that receives  the class creation data. This memory is allocated by this method. The caller must free this memory using <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> when it is no longer required.


## -returns



Returns a standard <b>HRESULT</b> value including the following.




## -see-also




<a href="https://msdn.microsoft.com/5c1551f7-f651-4b87-829a-ec9a07fb0ec2">DSCLASSCREATIONINFO</a>



<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/a6ac7006-73b8-4673-89d6-8285453481d3">IDsDisplaySpecifier</a>



<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>
 

 

