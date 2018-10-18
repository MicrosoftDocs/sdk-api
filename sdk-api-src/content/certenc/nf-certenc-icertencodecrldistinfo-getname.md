---
UID: NF:certenc.ICertEncodeCRLDistInfo.GetName
title: ICertEncodeCRLDistInfo::GetName
author: windows-sdk-content
description: Returns the name at a specified index of a certificate revocation list (CRL) distribution information point.
old-location: security\icertencodecrldistinfo_getname.htm
tech.root: seccrypto
ms.assetid: a564af61-fb5e-46b7-a818-333b4d5e2f25
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security],GetName method, GetName, GetName method [Security], GetName method [Security],CCertEncodeCRLDistInfo object, GetName method [Security],ICertEncodeCRLDistInfo interface, ICertEncodeCRLDistInfo interface [Security],GetName method, ICertEncodeCRLDistInfo.GetName, ICertEncodeCRLDistInfo::GetName, _certsrv_icertencodecrldistinfo_getname, certenc/ICertEncodeCRLDistInfo::GetName, security.icertencodecrldistinfo_getname
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
 - ICertEncodeCRLDistInfo.GetName
 - CCertEncodeCRLDistInfo.GetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeCRLDistInfo::GetName


## -description


The <b>GetName</b> method returns the name at a specified index of a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate revocation list</a> (CRL) distribution information point.


## -parameters




### -param DistPointIndex [in]

Specifies the index of the distribution point for which to get a name. The first value is at index zero.


### -param NameIndex [in]

Specifies the index of the name entry to get. The first value is at index zero.


### -param pstrName

TBD




#### - pbstrName [out]

A pointer to a <b>BSTR</b> that represents the name value. When you have finished using the <b>BSTR</b>, free it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the name at the specified index of the specified distribution point. The return value is a <a href="https://msdn.microsoft.com/en-us/library/ms721629(v=VS.85).aspx">Unicode</a> string.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383911(v=VS.85).aspx">ICertEncodeCRLDistInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383963(v=VS.85).aspx">ICertEncodeCRLDistInfo::GetNameCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383985(v=VS.85).aspx">ICertEncodeCRLDistInfo::SetNameEntry</a>
 

 

