---
UID: NF:credentialprovider.ICredentialProviderUserArray.GetCount
title: ICredentialProviderUserArray::GetCount (credentialprovider.h)
author: windows-sdk-content
description: Retrieves the number of ICredentialProviderUser objects in the user array.
old-location: shell\ICredentialProviderUserArray_GetCount.htm
tech.root: shell
ms.assetid: 524A9FA1-5106-42d2-A4B6-5D3B83E3A6BA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Windows Shell], GetCount method [Windows Shell],ICredentialProviderUserArray interface, ICredentialProviderUserArray interface [Windows Shell],GetCount method, ICredentialProviderUserArray.GetCount, ICredentialProviderUserArray::GetCount, credentialprovider/ICredentialProviderUserArray::GetCount, shell.ICredentialProviderUserArray_GetCount
ms.topic: method
f1_keywords: ["credentialprovider/ICredentialProviderUserArray.GetCount"]
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CredentialProvider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: CredentialProvider.lib
req.dll: Authui.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Authui.dll
api_name:
 - ICredentialProviderUserArray.GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICredentialProviderUserArray::GetCount


## -description


Retrieves the number of <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruser">ICredentialProviderUser</a> objects in the user array.


## -parameters




### -param userCount [out]

A pointer to a value that, when this method returns successfully, receives the number of users in the array.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruserarray">ICredentialProviderUserArray</a>
 

 

