---
UID: NF:davclnt.DavDeleteConnection
title: DavDeleteConnection function
author: windows-sdk-content
description: Closes a connection that was created by using the DavAddConnection function.
old-location: webdav\davdeleteconnection.htm
old-project: webdav
ms.assetid: 736b8a16-30db-410e-8295-97730297d04b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DavDeleteConnection, DavDeleteConnection function [WebDAV], davclnt/DavDeleteConnection, webdav.davdeleteconnection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: davclnt.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: AUTHNEXTSTEP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - netapi32.dll
 - DavHlpr.dll
 - Ext-MS-Win-Rdr-DavHlpr-L1-1-0.dll
api_name:
 - DavDeleteConnection
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
---

# DavDeleteConnection function


## -description


Closes a connection that was created by using the <a href="https://msdn.microsoft.com/d69cba04-503c-4d21-b762-3094c0921e28">DavAddConnection</a> function.


## -parameters




### -param ConnectionHandle [in]

A handle to an open connection that was  created by using the  <a href="https://msdn.microsoft.com/d69cba04-503c-4d21-b762-3094c0921e28">DavAddConnection</a> function.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/a93fdd65-359e-4046-910d-347c3af01280">CertCloseStore</a>
 

 

