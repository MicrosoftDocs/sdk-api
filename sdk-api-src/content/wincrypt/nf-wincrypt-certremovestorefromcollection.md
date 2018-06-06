---
UID: NF:wincrypt.CertRemoveStoreFromCollection
title: CertRemoveStoreFromCollection function
author: windows-sdk-content
description: Removes a sibling certificate store from a collection store.
old-location: security\certremovestorefromcollection.htm
old-project: SecCrypto
ms.assetid: e1564848-8b39-4ea9-9148-142ceaaaed15
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CertRemoveStoreFromCollection, CertRemoveStoreFromCollection function [Security], _crypto2_certremovestorefromcollection, security.certremovestorefromcollection, wincrypt/CertRemoveStoreFromCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertRemoveStoreFromCollection
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertRemoveStoreFromCollection function


## -description


The <b>CertRemoveStoreFromCollection</b> function removes a sibling <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> from a collection store.


## -parameters




### -param hCollectionStore [in]

A handle of the collection certificate store.


### -param hSiblingStore [in]

Handle of the sibling certificate store to be removed from the collection store.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/ea848d74-c3ec-4166-90ea-121b33f7f318">CertAddStoreToCollection</a>



<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a>



<a href="cryptography_functions.htm">Certificate Store Functions</a>
 

 

