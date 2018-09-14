---
UID: NF:certif.ICertServerExit.EnumerateAttributes
title: ICertServerExit::EnumerateAttributes
author: windows-sdk-content
description: Returns the name of the next request attribute within the current context, then increments the internal pointer to the following attribute.
old-location: security\icertserverexit_enumerateattributes.htm
tech.root: seccrypto
ms.assetid: df778207-3b20-45a5-a705-8dba566eb658
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: CCertServerExit object [Security],EnumerateAttributes method, EnumerateAttributes, EnumerateAttributes method [Security], EnumerateAttributes method [Security],CCertServerExit object, EnumerateAttributes method [Security],ICertServerExit interface, ICertServerExit interface [Security],EnumerateAttributes method, ICertServerExit.EnumerateAttributes, ICertServerExit::EnumerateAttributes, _certsrv_icertserverexit_enumerateattributes, certif/ICertServerExit::EnumerateAttributes, security.icertserverexit_enumerateattributes
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
 - ICertServerExit.EnumerateAttributes
 - CCertServerExit.EnumerateAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertServerExit::EnumerateAttributes


## -description


The <b>EnumerateAttributes</b> method returns the name of the next request attribute within the current context, then increments the internal pointer to the following <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a>.

Before calling <b>EnumerateAttributes</b>, an application calls 
<a href="https://msdn.microsoft.com/c81b9c4d-483e-48b8-a270-f570e148d371">ICertServerExit::EnumerateAttributesSetup</a>. When done enumerating, an application calls 
<a href="https://msdn.microsoft.com/6ac7afbb-49c6-45b3-a27e-5ba995684848">ICertServerExit::EnumerateAttributesClose</a>.


## -parameters




### -param pstrAttributeName [out]

A pointer to the enumerated attribute name.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and *<i>pstrAttributeName</i> is set to the <b>BSTR</b> that contains the name of the enumerated <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a>. A value of S_FALSE is returned if the last attribute was already enumerated.

To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrAttributeName</i>.

When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a string that contains the name of the enumerated attribute, or an empty string if the last attribute was already enumerated.




## -see-also




<a href="https://msdn.microsoft.com/1554c09c-a7c1-44ad-9821-93c0913212fc">ICertServerExit</a>



<a href="https://msdn.microsoft.com/6ac7afbb-49c6-45b3-a27e-5ba995684848">ICertServerExit::EnumerateAttributesClose</a>



<a href="https://msdn.microsoft.com/c81b9c4d-483e-48b8-a270-f570e148d371">ICertServerExit::EnumerateAttributesSetup</a>



<a href="https://msdn.microsoft.com/894bde77-5e76-452b-acf5-c73fcaf1fa31">ICertServerExit::GetRequestAttribute</a>
 

 

