---
UID: NF:slpublic.SLAcquireGenuineTicket
title: SLAcquireGenuineTicket function (slpublic.h)
author: windows-sdk-content
description: Gets a XrML genuine ticket acquired from the Software Licensing Server (SLS).
old-location: security\slacquiregenuineticket.htm
tech.root: SecSLApi
ms.assetid: 028099c8-9116-4212-bc29-1065b22be593
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SLAcquireGenuineTicket, SLAcquireGenuineTicket function [Security], security.slacquiregenuineticket, slpublic/SLAcquireGenuineTicket
ms.topic: function
req.header: slpublic.h
req.include-header: 
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
req.lib: Slcext.lib
req.dll: Slcext.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Slcext.dll
api_name:
 - SLAcquireGenuineTicket
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SLAcquireGenuineTicket function


## -description


Gets a XrML genuine ticket acquired from the Software Licensing Server (SLS).


## -parameters




### -param ppTicketBlob [out]

The address of a pointer to a buffer that receives the ticket BLOB. When you have finished using this buffer, free it by calling the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


### -param pcbTicketBlob [out]

A pointer to the size, in bytes, of the <i>ppTicketBlob</i> buffer.


### -param pwszTemplateId [in]

A pointer to a null-terminated string that contains the ID of the BLOB template stored on the SLS.


### -param pwszServerUrl [in]

A pointer to a null-terminated string that contains the URL of the SLS.


### -param pwszClientToken [in, optional]

Reserved.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



