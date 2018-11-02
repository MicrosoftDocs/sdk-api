---
UID: NF:azroles.IAzAuthorizationStore2.CreateApplication2
title: IAzAuthorizationStore2::CreateApplication2
author: windows-sdk-content
description: Creates an IAzApplication2 object by using the specified name.
old-location: security\iazauthorizationstore2_createapplication2.htm
tech.root: secauthz
ms.assetid: d9af40e4-9ed9-4b81-b808-315eef07a96d
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CreateApplication2, CreateApplication2 method [Security], CreateApplication2 method [Security],IAzAuthorizationStore2 interface, IAzAuthorizationStore2 interface [Security],CreateApplication2 method, IAzAuthorizationStore2.CreateApplication2, IAzAuthorizationStore2::CreateApplication2, azroles/IAzAuthorizationStore2::CreateApplication2, security.iazauthorizationstore2_createapplication2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzAuthorizationStore2.CreateApplication2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzAuthorizationStore2::CreateApplication2


## -description


The <b>CreateApplication2</b> method creates an <a href="https://msdn.microsoft.com/en-us/library/Aa446685(v=VS.85).aspx">IAzApplication2</a> object by using the specified name.


## -parameters




### -param bstrApplicationName [in]

The name for the new <a href="https://msdn.microsoft.com/en-us/library/Aa446685(v=VS.85).aspx">IAzApplication2</a> object.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppApplication [out]

A pointer to a pointer to the created <a href="https://msdn.microsoft.com/en-us/library/Aa446685(v=VS.85).aspx">IAzApplication2</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



You must call the <a href="https://msdn.microsoft.com/en-us/library/Aa377565(v=VS.85).aspx">IAzApplication::Submit</a> method to persist any changes made by the returned object.

The returned <a href="https://msdn.microsoft.com/en-us/library/Aa446685(v=VS.85).aspx">IAzApplication2</a> object is an immediate child object of the <a href="https://msdn.microsoft.com/en-us/library/Aa377582(v=VS.85).aspx">IAzAuthorizationStore2</a> object.



