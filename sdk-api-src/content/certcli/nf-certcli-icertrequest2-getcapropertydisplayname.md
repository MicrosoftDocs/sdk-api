---
UID: NF:certcli.ICertRequest2.GetCAPropertyDisplayName
title: ICertRequest2::GetCAPropertyDisplayName
author: windows-sdk-content
description: Retrieves the property display name for a certification authority (CA) property.
old-location: security\icertrequest2_getcapropertydisplayname.htm
tech.root: seccrypto
ms.assetid: 5c294758-b2aa-497b-8377-6c5987576f82
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CCertRequest object [Security],GetCAPropertyDisplayName method, GetCAPropertyDisplayName, GetCAPropertyDisplayName method [Security], GetCAPropertyDisplayName method [Security],CCertRequest object, GetCAPropertyDisplayName method [Security],ICertRequest interface, GetCAPropertyDisplayName method [Security],ICertRequest2 interface, GetCAPropertyDisplayName method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetCAPropertyDisplayName method, ICertRequest2 interface [Security],GetCAPropertyDisplayName method, ICertRequest2.GetCAPropertyDisplayName, ICertRequest2::GetCAPropertyDisplayName, ICertRequest3 interface [Security],GetCAPropertyDisplayName method, ICertRequest3::GetCAPropertyDisplayName, ICertRequest::GetCAPropertyDisplayName, _certsrv_icertrequest2_getcapropertydisplayname, certcli/ICertRequest2::GetCAPropertyDisplayName, certcli/ICertRequest3::GetCAPropertyDisplayName, certcli/ICertRequest::GetCAPropertyDisplayName, security.icertrequest2_getcapropertydisplayname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certcli.h
req.include-header: Certsrv.h
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
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertRequest3.GetCAPropertyDisplayName
 - ICertRequest2.GetCAPropertyDisplayName
 - ICertRequest.GetCAPropertyDisplayName
 - CCertRequest.GetCAPropertyDisplayName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertRequest2::GetCAPropertyDisplayName


## -description


The <b>GetCAPropertyDisplayName</b> method retrieves the property display name for a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) property.


## -parameters




### -param strConfig [in]

Represents a valid configuration string for the CA in the form <i>ComputerName</i><b>\</b><i>CAName</i>, where <i>ComputerName</i> is the network name of the Certificate Services server, and <i>CAName</i> is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa383268(v=VS.85).aspx">ICertConfig</a>.


### -param PropId [in]

Specifies the property identifier. For information about this parameter, see the table in 
<a href="https://msdn.microsoft.com/en-us/library/Aa383238(v=VS.85).aspx">ICertAdmin2::GetCAProperty</a>.


### -param pstrDisplayName [out, retval]

A pointer to the <b>BSTR</b> that represents the property's display name. When you have finished using the <b>BSTR</b>, free it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is a <b>String</b> that contains the property's display name.




## -remarks



The <b>GetCAPropertyDisplayName</b> method's functionality is similar to that of the <a href="https://msdn.microsoft.com/en-us/library/Aa383239(v=VS.85).aspx">ICertAdmin2::GetCAPropertyDisplayName</a> method. 

In the ICertAdmin2 method, the CA enforces that the caller has CA read access, which is usually only granted to CA officers and CA administrators.

By contrast, in the ICertRequest2 and ICertRequest3 implementations of the method, the CA does not require any access rights by default.  Only Distributed Component Object Model (DCOM) <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">access control lists</a> (ACLs) are enforced; for a domain-joined CA, the DCOM ACLs allow Everyone access to the CAs.  Everyone does not include Anonymous.
The CA's request interface can be locked down by using the registry configuration to enforce that the caller has enroll access.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa385040(v=VS.85).aspx">CCertRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385040(v=VS.85).aspx">ICertRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee373776(v=VS.85).aspx">ICertRequest3</a>
 

 

