---
UID: NF:certenc.ICertEncodeCRLDistInfo.SetNameCount
title: ICertEncodeCRLDistInfo::SetNameCount
author: windows-sdk-content
description: Sets a name count for the specified distribution point in a certificate revocation list (CRL) distribution information array.
old-location: security\icertencodecrldistinfo_setnamecount.htm
old-project: seccrypto
ms.assetid: ce27adfd-e21a-4e8d-882e-72041f97958a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security],SetNameCount method, ICertEncodeCRLDistInfo interface [Security],SetNameCount method, ICertEncodeCRLDistInfo.SetNameCount, ICertEncodeCRLDistInfo::SetNameCount, SetNameCount, SetNameCount method [Security], SetNameCount method [Security],CCertEncodeCRLDistInfo object, SetNameCount method [Security],ICertEncodeCRLDistInfo interface, _certsrv_icertencodecrldistinfo_setnamecount, certenc/ICertEncodeCRLDistInfo::SetNameCount, security.icertencodecrldistinfo_setnamecount
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509EnrollmentAuthFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeCRLDistInfo.SetNameCount
 - CCertEncodeCRLDistInfo.SetNameCount
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# ICertEncodeCRLDistInfo::SetNameCount


## -description


The <b>SetNameCount</b> method sets a name count for the specified distribution point in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) distribution information array.


## -parameters




### -param DistPointIndex [in]

Specifies the index of the distribution point for which to set the name count.


### -param NameCount [in]

Specifies the name count.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/e9c0053f-263f-4d7b-9356-bc33af989dbe">ICertEncodeCRLDistInfo</a>



<a href="https://msdn.microsoft.com/64102b89-defe-4f26-b6b2-8c3903e08347">ICertEncodeCRLDistInfo::GetNameCount</a>



<a href="https://msdn.microsoft.com/fe33265a-8c75-4e16-8178-3569cf30d8e4">ICertEncodeCRLDistInfo::SetNameEntry</a>
 

 

