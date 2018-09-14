---
UID: NF:shlwapi.IUnknown_QueryService
title: IUnknown_QueryService function
author: windows-sdk-content
description: Retrieves an interface for a service from a specified object.
old-location: shell\IUnknown_QueryService.htm
tech.root: shell
ms.assetid: 3e3f3ed0-ad36-40ef-b30c-8c85ff159f21
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IUnknown_QueryService, IUnknown_QueryService function [Windows Shell], _shell_IUnknown_QueryService, shell.IUnknown_QueryService, shlwapi/IUnknown_QueryService
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
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
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-shlwapi-IE-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-comhelpers-l1-1-0.dll
api_name:
 - IUnknown_QueryService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUnknown_QueryService function


## -description


Retrieves an interface for a service from a specified object.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> instance of the COM object that supports the service.


### -param guidService [in]

Type: <b>REFGUID</b>

The service's unique identifier (SID).


### -param riid [in]

Type: <b>REFIID</b>

The IID of the desired service interface.


### -param ppvOut [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested <i>riid</i>. If successful, the calling application is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> using this value when the service is no longer needed. In the case of failure, this value is <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful. Returns <b>E_FAIL</b> if the object does not support <a href="https://msdn.microsoft.com/library/Cc678965(v=VS.85).aspx">IServiceProvider</a>. Otherwise, the function returns the <b>HRESULT</b> returned by the object's <a href="https://msdn.microsoft.com/library/Cc678966(v=VS.85).aspx">QueryService</a> method.




## -remarks



If the object passed in the <i>punk</i> parameter supports the <a href="https://msdn.microsoft.com/library/Cc678965(v=VS.85).aspx">IServiceProvider</a> interface, then its <a href="https://msdn.microsoft.com/library/Cc678966(v=VS.85).aspx">QueryService</a> method is invoked, passing the <i>guidService</i>, <i>riid</i>, and <i>ppvOut</i> parameters and propagating the return value. Otherwise, the function returns E_FAIL.

For those versions of Windows that do not include <b>IUnknown_QueryService</b> in Shlwapi.h, this function must be called directly from Shlwapi.dll using ordinal 176.




## -see-also




<a href="https://msdn.microsoft.com/library/Cc678965(v=VS.85).aspx">IServiceProvider</a>



<a href="https://msdn.microsoft.com/library/Cc678966(v=VS.85).aspx">QueryService</a>
 

 

