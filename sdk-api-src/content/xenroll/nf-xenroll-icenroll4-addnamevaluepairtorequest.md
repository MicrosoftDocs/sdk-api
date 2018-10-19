---
UID: NF:xenroll.ICEnroll4.addNameValuePairToRequest
title: ICEnroll4::addNameValuePairToRequest
author: windows-sdk-content
description: Adds an unauthenticated name-value string pair to the request. This method was first defined in the ICEnroll4 interface.
old-location: security\icenroll4_addnamevaluepairtorequest.htm
tech.root: seccrypto
ms.assetid: 252d1789-1207-4281-b044-e1f1ca6cd585
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CEnroll object [Security],addNameValuePairToRequest method, ICEnroll4 interface [Security],addNameValuePairToRequest method, ICEnroll4.addNameValuePairToRequest, ICEnroll4::addNameValuePairToRequest, _xen_icenroll4_addnamevaluepairtorequest, addNameValuePairToRequest, addNameValuePairToRequest method [Security], addNameValuePairToRequest method [Security],CEnroll object, addNameValuePairToRequest method [Security],ICEnroll4 interface, security.icenroll4_addnamevaluepairtorequest, xenroll/ICEnroll4::addNameValuePairToRequest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.addNameValuePairToRequest
 - CEnroll.addNameValuePairToRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll4::addNameValuePairToRequest


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addNameValuePairToRequest</b> method adds an unauthenticated name-value string pair to the request. This method was first defined in the <a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a> interface.


## -parameters




### -param Flags [in]

This parameter is reserved for future use and must be set to zero.


### -param strName [in]

The name portion of the name-value pair.


### -param strValue [in]

The value portion of the name-value pair.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



