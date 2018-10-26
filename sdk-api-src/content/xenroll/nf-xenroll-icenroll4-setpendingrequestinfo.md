---
UID: NF:xenroll.ICEnroll4.setPendingRequestInfo
title: ICEnroll4::setPendingRequestInfo
author: windows-sdk-content
description: Sets properties for a pending request. This method was first defined in the ICEnroll4 interface.
old-location: security\icenroll4_setpendingrequestinfo.htm
tech.root: seccrypto
ms.assetid: be369059-5852-4cde-8f78-d5883735b670
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CEnroll object [Security],setPendingRequestInfo method, ICEnroll4 interface [Security],setPendingRequestInfo method, ICEnroll4.setPendingRequestInfo, ICEnroll4::setPendingRequestInfo, _xen_icenroll4_setpendingrequestinfo, security.icenroll4_setpendingrequestinfo, setPendingRequestInfo, setPendingRequestInfo method [Security], setPendingRequestInfo method [Security],CEnroll object, setPendingRequestInfo method [Security],ICEnroll4 interface, xenroll/ICEnroll4::setPendingRequestInfo
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
 - ICEnroll4.setPendingRequestInfo
 - CEnroll.setPendingRequestInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll4::setPendingRequestInfo


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>setPendingRequestInfo</b> method sets properties for a pending request. This method was first defined in the <a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a> interface.


## -parameters




### -param lRequestID [in]

An identifier for the request, as assigned by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a>.


### -param strCADNS [in]

The Domain Name System (DNS) name of the certification authority. The  <i>strCADNS</i> parameter cannot be <b>NULL</b>.


### -param strCAName [in]

The name of the certification authority. The <i>strCAName</i> parameter cannot be <b>NULL</b>.


### -param strFriendlyName [in]

The display name of the certification authority. The <i>strFriendlyName</i> parameter can be <b>NULL</b>.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



