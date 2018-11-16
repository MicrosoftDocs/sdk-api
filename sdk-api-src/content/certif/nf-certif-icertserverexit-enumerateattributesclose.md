---
UID: NF:certif.ICertServerExit.EnumerateAttributesClose
title: ICertServerExit::EnumerateAttributesClose
author: windows-sdk-content
description: Frees any resources connected with attribute enumeration.
old-location: security\icertserverexit_enumerateattributesclose.htm
tech.root: SecCrypto
ms.assetid: 6ac7afbb-49c6-45b3-a27e-5ba995684848
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CCertServerExit object [Security],EnumerateAttributesClose method, EnumerateAttributesClose, EnumerateAttributesClose method [Security], EnumerateAttributesClose method [Security],CCertServerExit object, EnumerateAttributesClose method [Security],ICertServerExit interface, ICertServerExit interface [Security],EnumerateAttributesClose method, ICertServerExit.EnumerateAttributesClose, ICertServerExit::EnumerateAttributesClose, _certsrv_icertserverexit_enumerateattributesclose, certif/ICertServerExit::EnumerateAttributesClose, security.icertserverexit_enumerateattributesclose
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certif.h
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
 - ICertServerExit.EnumerateAttributesClose
 - CCertServerExit.EnumerateAttributesClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certif.h
: 
- ICertServerExit.EnumerateAttributesClose
: 
---

# ICertServerExit::EnumerateAttributesClose


## -description


The <b>EnumerateAttributesClose</b> method frees any resources connected with <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a> enumeration.

All applications that use 
<a href="https://msdn.microsoft.com/c81b9c4d-483e-48b8-a270-f570e148d371">ICertServerExit::EnumerateAttributesSetup</a> or 
<a href="https://msdn.microsoft.com/df778207-3b20-45a5-a705-8dba566eb658">ICertServerExit::EnumerateAttributes</a> should call <b>EnumerateAttributesClose</b> when finished enumerating.


## -parameters






## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/1554c09c-a7c1-44ad-9821-93c0913212fc">ICertServerExit</a>



<a href="https://msdn.microsoft.com/df778207-3b20-45a5-a705-8dba566eb658">ICertServerExit::EnumerateAttributes</a>



<a href="https://msdn.microsoft.com/c81b9c4d-483e-48b8-a270-f570e148d371">ICertServerExit::EnumerateAttributesSetup</a>
 

 

