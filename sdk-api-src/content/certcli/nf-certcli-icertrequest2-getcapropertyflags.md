---
UID: NF:certcli.ICertRequest2.GetCAPropertyFlags
title: ICertRequest2::GetCAPropertyFlags
author: windows-sdk-content
description: Retrieves the property flags for a certification authority (CA) property.
old-location: security\icertrequest2_getcapropertyflags.htm
tech.root: seccrypto
ms.assetid: bdc6ab73-a0b4-44cd-9e46-c453dcb45a41
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CCertRequest object [Security],GetCAPropertyFlags method, GetCAPropertyFlags, GetCAPropertyFlags method [Security], GetCAPropertyFlags method [Security],CCertRequest object, GetCAPropertyFlags method [Security],ICertRequest interface, GetCAPropertyFlags method [Security],ICertRequest2 interface, GetCAPropertyFlags method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetCAPropertyFlags method, ICertRequest2 interface [Security],GetCAPropertyFlags method, ICertRequest2.GetCAPropertyFlags, ICertRequest2::GetCAPropertyFlags, ICertRequest3 interface [Security],GetCAPropertyFlags method, ICertRequest3::GetCAPropertyFlags, ICertRequest::GetCAPropertyFlags, _certsrv_icertrequest2_getcapropertyflags, certcli/ICertRequest2::GetCAPropertyFlags, certcli/ICertRequest3::GetCAPropertyFlags, certcli/ICertRequest::GetCAPropertyFlags, security.icertrequest2_getcapropertyflags
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
 - ICertRequest3.GetCAPropertyFlags
 - ICertRequest2.GetCAPropertyFlags
 - ICertRequest.GetCAPropertyFlags
 - CCertRequest.GetCAPropertyFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertRequest2::GetCAPropertyFlags


## -description


The <b>GetCAPropertyFlags</b> method retrieves the property flags for a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) property.


## -parameters




### -param strConfig [in]

Represents a valid configuration string for the CA in the form <i>ComputerName</i><b>\</b><i>CAName</i>, where <i>ComputerName</i> is the network name of the Certificate Services server, and <i>CAName</i> is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>.


### -param PropId [in]

Specifies the property identifier. For information about this parameter, see the table in 
<a href="https://msdn.microsoft.com/8eaa2e36-4358-4abd-a7c2-2c9768766597">ICertAdmin2::GetCAProperty</a>.


### -param pPropFlags [out, retval]

A pointer to a <b>LONG</b> value that represents the property flags.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is a <b>Long</b> that represents the property flags.




## -remarks



The <b>GetCAPropertyFlags</b> method's functionality is similar to that of the <a href="https://msdn.microsoft.com/6f38bea1-e278-4085-b321-05f6765cc676">ICertAdmin2::GetCAPropertyFlags</a> method. 

In the ICertAdmin2 method, the CA enforces that the caller has CA read access, which is usually only granted to CA officers and CA administrators.

By contrast, in the ICertRequest2 and ICertRequest3 implementations of the method, the CA does not require any access rights by default.  Only Distributed Component Object Model (DCOM) <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control lists</a> (ACLs) are enforced; for a domain-joined CA, the DCOM ACLs allow Everyone access to the CAs.  Everyone does not include Anonymous.
The CA's request interface can be locked down by using the registry configuration to enforce that the caller has enroll access.




## -see-also




<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">CCertRequest</a>



<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">ICertRequest</a>



<a href="https://msdn.microsoft.com/8587a682-27a5-4f26-b4bb-7088e4e5d8d3">ICertRequest2</a>



<a href="https://msdn.microsoft.com/01de2ac0-4844-41a6-acef-e3e83b350393">ICertRequest3</a>
 

 

