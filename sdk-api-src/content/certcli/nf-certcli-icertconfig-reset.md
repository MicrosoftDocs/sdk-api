---
UID: NF:certcli.ICertConfig.Reset
title: ICertConfig::Reset
author: windows-sdk-content
description: Resets the configuration query state to point at the Certificate Services server configuration indexed on the specified configuration point. This method was first defined in the ICertConfig interface.
old-location: security\icertconfig2_reset.htm
tech.root: seccrypto
ms.assetid: 62c24bda-463a-4238-be70-14e28bcbfb39
ms.author: windowssdkdev
ms.date: 10/05/2018
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
---

# ICertConfig::Reset


## -description


The <b>Reset</b> method resets the configuration query <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a> to point at the Certificate Services server configuration indexed on the specified configuration point. This method was first defined in the <a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a> interface.

Each individual configuration indicates a specific Certificate Services server. Some Certificate Services servers may have multiple valid configurations in the configuration database.


## -parameters




### -param Index [in]

Specifies the configuration point used by the configuration query to index a Certificate Services server configuration. The first configuration is index zero.


### -param pCount [out]

A pointer to the number of configurations in the enterprise.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and the <i>pCount</i> parameter points to a <b>Long</b> that contains the number of configurations in the enterprise.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of configurations in the enterprise.




## -see-also




<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>



<a href="https://msdn.microsoft.com/6bac5961-f9cc-4859-affa-aa7ed152ebfa">ICertConfig2</a>



<a href="https://msdn.microsoft.com/af81c25e-94e7-4c50-9e90-612c034e24b4">Next</a>
 

 

