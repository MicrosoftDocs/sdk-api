---
UID: NF:certenc.ICertEncodeCRLDistInfo.Reset
title: ICertEncodeCRLDistInfo::Reset
author: windows-sdk-content
description: Resets a certificate revocation list (CRL) distribution information array to a specified number of distribution point structures.
old-location: security\icertencodecrldistinfo_reset.htm
tech.root: seccrypto
ms.assetid: 899de888-918f-4202-a324-0e603eba2324
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security],Reset method, ICertEncodeCRLDistInfo interface [Security],Reset method, ICertEncodeCRLDistInfo.Reset, ICertEncodeCRLDistInfo::Reset, Reset, Reset method [Security], Reset method [Security],CCertEncodeCRLDistInfo object, Reset method [Security],ICertEncodeCRLDistInfo interface, _certsrv_icertencodecrldistinfo_reset, certenc/ICertEncodeCRLDistInfo::Reset, security.icertencodecrldistinfo_reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenc.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeCRLDistInfo.Reset
 - CCertEncodeCRLDistInfo.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeCRLDistInfo::Reset


## -description


The <b>Reset</b> method resets a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) distribution information array to a specified number of distribution point structures.

 The values of all the elements in the array of structures are set to zero.


## -parameters




### -param DistPointCount [in]

Specifies the number of CRL distribution points in the CRL distribution information array.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/e9c0053f-263f-4d7b-9356-bc33af989dbe">ICertEncodeCRLDistInfo</a>



<a href="https://msdn.microsoft.com/8c7d0d14-e755-4223-8cd5-0ebc784960cf">ICertEncodeCRLDistInfo::GetDistPointCount</a>
 

 

