---
UID: NF:certif.ICertServerExit.SetContext
title: ICertServerExit::SetContext
author: windows-sdk-content
description: Causes the current instantiation of the interface to operate on the request referenced by Context.
old-location: security\icertserverexit_setcontext.htm
tech.root: seccrypto
ms.assetid: 8d317114-17bd-4b22-8e37-99db72740538
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CCertServerExit object [Security],SetContext method, ICertServerExit interface [Security],SetContext method, ICertServerExit.SetContext, ICertServerExit::SetContext, SetContext, SetContext method [Security], SetContext method [Security],CCertServerExit object, SetContext method [Security],ICertServerExit interface, _certsrv_icertserverexit_setcontext, certif/ICertServerExit::SetContext, security.icertserverexit_setcontext
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
 - ICertServerExit.SetContext
 - CCertServerExit.SetContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertServerExit::SetContext


## -description


The <b>SetContext</b> method causes the current instantiation of the interface to operate on the request referenced by <i>Context</i>.

This must be identical to a value given by the <i>Context</i> parameter in 
<a href="https://msdn.microsoft.com/ebe4ef0c-5778-4a62-b112-9b16b250814f">ICertExit::Notify</a>. This method must be called before calling any of the other 
<a href="https://msdn.microsoft.com/1554c09c-a7c1-44ad-9821-93c0913212fc">ICertServerExit</a> methods, in order that the interface reference a valid request.


## -parameters




### -param Context [in]

Specifies the request and associated certificate under construction.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/ebe4ef0c-5778-4a62-b112-9b16b250814f">ICertExit::Notify</a>



<a href="https://msdn.microsoft.com/860f0eb0-5b23-44bd-8416-687a94962f1b">ICertPolicy::VerifyRequest</a>



<a href="https://msdn.microsoft.com/1554c09c-a7c1-44ad-9821-93c0913212fc">ICertServerExit</a>
 

 

