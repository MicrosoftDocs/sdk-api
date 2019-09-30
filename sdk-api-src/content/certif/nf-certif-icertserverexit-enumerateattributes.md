---
UID: NF:certif.ICertServerExit.EnumerateAttributes
title: ICertServerExit::EnumerateAttributes (certif.h)
author: windows-sdk-content
description: Returns the name of the next request attribute within the current context, then increments the internal pointer to the following attribute.
old-location: security\icertserverexit_enumerateattributes.htm
tech.root: SecCrypto
ms.assetid: df778207-3b20-45a5-a705-8dba566eb658
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CCertServerExit object [Security],EnumerateAttributes method, EnumerateAttributes, EnumerateAttributes method [Security], EnumerateAttributes method [Security],CCertServerExit object, EnumerateAttributes method [Security],ICertServerExit interface, ICertServerExit interface [Security],EnumerateAttributes method, ICertServerExit.EnumerateAttributes, ICertServerExit::EnumerateAttributes, _certsrv_icertserverexit_enumerateattributes, certif/ICertServerExit::EnumerateAttributes, security.icertserverexit_enumerateattributes
ms.topic: method
f1_keywords: 
 - "certif/ICertServerExit.EnumerateAttributes"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertServerExit::EnumerateAttributes


## -description


The <b>EnumerateAttributes</b> method returns the name of the next request attribute within the current context, then increments the internal pointer to the following <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">attribute</a>.

Before calling <b>EnumerateAttributes</b>, an application calls 
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateattributessetup">ICertServerExit::EnumerateAttributesSetup</a>. When done enumerating, an application calls 
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateattributesclose">ICertServerExit::EnumerateAttributesClose</a>.


## -parameters




### -param pstrAttributeName [out]

A pointer to the enumerated attribute name.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and *<i>pstrAttributeName</i> is set to the <b>BSTR</b> that contains the name of the enumerated <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">attribute</a>. A value of S_FALSE is returned if the last attribute was already enumerated.

To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrAttributeName</i>.

When you have finished using the <b>BSTR</b>, free it by calling the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a string that contains the name of the enumerated attribute, or an empty string if the last attribute was already enumerated.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateattributesclose">ICertServerExit::EnumerateAttributesClose</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateattributessetup">ICertServerExit::EnumerateAttributesSetup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-getrequestattribute">ICertServerExit::GetRequestAttribute</a>
 

 

