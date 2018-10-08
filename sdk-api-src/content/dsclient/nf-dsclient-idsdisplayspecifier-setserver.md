---
UID: NF:dsclient.IDsDisplaySpecifier.SetServer
title: IDsDisplaySpecifier::SetServer
author: windows-sdk-content
description: Specifies the server from which display specifier data is obtained.
old-location: ad\idsdisplayspecifier_setserver.htm
tech.root: ad
ms.assetid: f72cc711-7dec-4f5a-9cf1-57612240b435
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: DSSSF_DONTSIGNSEAL, DSSSF_DSAVAILABLE, DSSSF_SIMPLEAUTHENTICATE, IDsDisplaySpecifier interface [Active Directory],SetServer method, IDsDisplaySpecifier.SetServer, IDsDisplaySpecifier::SetServer, SetServer, SetServer method [Active Directory], SetServer method [Active Directory],IDsDisplaySpecifier interface, _glines_idsdisplayspecifier_setserver, ad.idsdisplayspecifier__setserver, ad.idsdisplayspecifier_setserver, dsclient/IDsDisplaySpecifier::SetServer
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDsDisplaySpecifier.SetServer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsDisplaySpecifier::SetServer


## -description


The <b>IDsDisplaySpecifier::SetServer</b> method specifies the server from which display specifier data is obtained.


## -parameters




### -param pszServer [in]

Pointer to a null-terminated Unicode string that contains the name of the server that will be used to obtain the display specifier data.


### -param pszUserName [in]

Pointer to a null-terminated Unicode string that contains the user name to be used for access to the server specified in <i>pszServer</i>.


### -param pszPassword [in]

Pointer to a null-terminated Unicode string that contains the password used to access the server specified in <i>pszServer</i>.


### -param dwFlags [in]

Contains a set of flags used to bind to the directory service. This can be zero or a combination of one or more of the following values.



#### DSSSF_SIMPLEAUTHENTICATE (1 (0x1))

The <a href="https://msdn.microsoft.com/a6ac7006-73b8-4673-89d6-8285453481d3">IDsDisplaySpecifier</a> object uses simple authentication instead of secure authentication.



#### DSSSF_DONTSIGNSEAL (2 (0x2))

The <a href="https://msdn.microsoft.com/a6ac7006-73b8-4673-89d6-8285453481d3">IDsDisplaySpecifier</a> object does not use signing and sealing when opening objects.



#### DSSSF_DSAVAILABLE (2147483648 (0x80000000))

The <a href="https://msdn.microsoft.com/a6ac7006-73b8-4673-89d6-8285453481d3">IDsDisplaySpecifier</a> object will not check whether the directory server is available.


## -returns



Returns a standard <b>HRESULT</b> value including the following.




## -remarks



The server data is cached by the <a href="https://msdn.microsoft.com/a6ac7006-73b8-4673-89d6-8285453481d3">IDsDisplaySpecifier</a> object. The <b>IDsDisplaySpecifier</b> object does not actually bind to the server until a specific method, such as <a href="https://msdn.microsoft.com/c4fc25f6-0157-406d-b523-8542183291ed">IDsDisplaySpecifier::GetDisplaySpecifier</a>,  is called.




## -see-also




<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/a6ac7006-73b8-4673-89d6-8285453481d3">IDsDisplaySpecifier</a>



<a href="https://msdn.microsoft.com/c4fc25f6-0157-406d-b523-8542183291ed">IDsDisplaySpecifier::GetDisplaySpecifier</a>
 

 

