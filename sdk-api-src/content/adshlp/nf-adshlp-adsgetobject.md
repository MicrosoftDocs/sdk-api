---
UID: NF:adshlp.ADsGetObject
title: ADsGetObject function
author: windows-sdk-content
description: Binds to an object given its path and a specified interface identifier.
old-location: adsi\adsgetobject.htm
old-project: ADSI
ms.assetid: 595b2c7f-584c-4343-a75c-327d8ed4ceb1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ADsGetObject, ADsGetObject function [ADSI], _ds_adsgetobject, adshlp/ADsGetObject, adsi.adsgetobject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: adshlp.h
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
tech.root: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - ADsGetObject
product: Windows
targetos: Windows
req.lib: Activeds.lib
req.dll: Activeds.dll
req.irql: 
---

# ADsGetObject function


## -description


The <b>ADsGetObject</b> function binds to an object given its path and a specified interface identifier.


## -parameters




### -param lpszPathName [in]

Type: <b>LPCWSTR</b>

The null-terminated Unicode string that specifies the path  used to bind to the object in the underlying directory service. For more information and code examples for binding strings for this parameter, see  <a href="https://msdn.microsoft.com/adacf6af-8683-4c3c-91bf-9489f2d5d817">LDAP ADsPath</a> and  <a href="https://msdn.microsoft.com/0fad4b34-5287-43a0-a172-a08955b8b132">WinNT ADsPath</a>.


### -param riid [in]

Type: <b>REFIID</b>

Interface identifier for a specified interface on this object.


### -param ppObject [out]

Type: <b>VOID**</b>

Pointer to a pointer to the requested Interface.


## -returns



Type: <b>HRESULT</b>

This method supports the standard <b>HRESULT</b> return values, as well as the following.

For more information about other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



A C/C++ client calls the <b>ADsGetObject</b> helper function to bind to an ADSI object. It is equivalent to a Visual Basic client calling the <a href="https://msdn.microsoft.com/15d8116a-8ec1-48b5-bf62-411fdff7c8b8">GetObject</a> function. They both take an ADsPath as input and returns a pointer to the requested interface. By default the binding uses ADS_SECURE_AUTHENTICATION option with the security context of the calling thread. However, if the authentication fails, the secure bind is downgraded to an anonymous bind, for example, a simple bind without user credentials. To securely bind to an ADSI object, use the <a href="https://msdn.microsoft.com/c4b85d8e-b33b-47a4-b7d7-5f901f80dce9">ADsOpenObject</a> function instead of the  <b>ADsGetObject</b> function.

For a code example that shows how to use <a href="https://msdn.microsoft.com/c4b85d8e-b33b-47a4-b7d7-5f901f80dce9">ADsOpenObject</a>, see <a href="https://msdn.microsoft.com/15d8116a-8ec1-48b5-bf62-411fdff7c8b8">Binding With GetObject and ADsGetObject</a>.

It is possible to bind to an ADSI object with a user credential different from that of the currently logged-on user. To perform this operation, use the   <a href="https://msdn.microsoft.com/c4b85d8e-b33b-47a4-b7d7-5f901f80dce9">ADsOpenObject</a> function.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/c4b85d8e-b33b-47a4-b7d7-5f901f80dce9">ADsOpenObject</a>



<a href="https://msdn.microsoft.com/15d8116a-8ec1-48b5-bf62-411fdff7c8b8">Binding With GetObject and ADsGetObject</a>
 

 

