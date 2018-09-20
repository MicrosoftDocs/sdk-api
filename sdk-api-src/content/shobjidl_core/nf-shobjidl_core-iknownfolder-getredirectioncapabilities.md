---
UID: NF:shobjidl_core.IKnownFolder.GetRedirectionCapabilities
title: IKnownFolder::GetRedirectionCapabilities
author: windows-sdk-content
description: Gets a value that states whether the known folder can have its path set to a new value or what specific restrictions or prohibitions are placed on that redirection.
old-location: shell\IKnownFolder_GetRedirectionCapabilities.htm
tech.root: shell
ms.assetid: 5abc4944-1fd7-400a-817d-b58a7f4989ea
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: GetRedirectionCapabilities, GetRedirectionCapabilities method [Windows Shell], GetRedirectionCapabilities method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetRedirectionCapabilities method, IKnownFolder.GetRedirectionCapabilities, IKnownFolder::GetRedirectionCapabilities, _shell_IKnownFolder_GetRedirectionCapabilities, shell.IKnownFolder_GetRedirectionCapabilities, shobjidl_core/IKnownFolder::GetRedirectionCapabilities
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IKnownFolder.GetRedirectionCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKnownFolder::GetRedirectionCapabilities


## -description


Gets a value that states whether the known folder can have its path set to a new value or what specific restrictions or prohibitions are placed on that redirection.


## -parameters




### -param pCapabilities [out]

Type: <b><a href="https://msdn.microsoft.com/3c9830fc-75cd-4b11-bfb4-55b66063614b">KF_REDIRECTION_CAPABILITIES</a>*</b>

When this method returns, contains a pointer to a <a href="https://msdn.microsoft.com/3c9830fc-75cd-4b11-bfb4-55b66063614b">KF_REDIRECTION_CAPABILITIES</a> value that indicates the redirection capabilities for this folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dbade93d-73f6-401b-9986-4e6fd439c874">IKnownFolder</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

