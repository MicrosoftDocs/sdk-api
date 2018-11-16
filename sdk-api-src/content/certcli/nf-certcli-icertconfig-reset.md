---
UID: NF:certcli.ICertConfig.Reset
title: ICertConfig::Reset
author: windows-sdk-content
description: Resets the configuration query state to point at the Certificate Services server configuration indexed on the specified configuration point. This method was first defined in the ICertConfig interface.
old-location: security\icertconfig2_reset.htm
tech.root: SecCrypto
ms.assetid: 62c24bda-463a-4238-be70-14e28bcbfb39
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CCertConfig object [Security],Reset method, ICertConfig interface [Security],Reset method, ICertConfig.Reset, ICertConfig2 interface [Security],Reset method, ICertConfig2::Reset, ICertConfig::Reset, Reset, Reset method [Security], Reset method [Security],CCertConfig object, Reset method [Security],ICertConfig interface, Reset method [Security],ICertConfig2 interface, _certsrv_icertconfig_reset, certcli/ICertConfig2::Reset, certcli/ICertConfig::Reset, security.icertconfig2_reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certcli.h
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
 - ICertConfig2.Reset
 - ICertConfig.Reset
 - CCertConfig.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certcli.h
: 
- ICertConfig.Reset
: 
---

# ICertConfig::Reset


## -description


The <b>Reset</b> method resets the configuration query <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">state</a> to point at the Certificate Services server configuration indexed on the specified configuration point. This method was first defined in the <a href="https://msdn.microsoft.com/en-us/library/Aa383268(v=VS.85).aspx">ICertConfig</a> interface.

Each individual configuration indicates a specific Certificate Services server. Some Certificate Services servers may have multiple valid configurations in the configuration database.


## -parameters




### -param Index [in]

Specifies the configuration point used by the configuration query to index a Certificate Services server configuration. The first configuration is index zero.


### -param pCount [out]

A pointer to the number of configurations in the enterprise.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and the <i>pCount</i> parameter points to a <b>Long</b> that contains the number of configurations in the enterprise.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of configurations in the enterprise.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383268(v=VS.85).aspx">ICertConfig</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383272(v=VS.85).aspx">ICertConfig2</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383280(v=VS.85).aspx">Next</a>
 

 

