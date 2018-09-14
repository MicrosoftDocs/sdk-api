---
UID: NF:xenroll.ICEnroll3.Reset
title: ICEnroll3::Reset
author: windows-sdk-content
description: Returns the certificate enrollment control object to its initial state and thereby allow reuse of the control. This method was first defined in the ICEnroll3 interface.
old-location: security\icenroll4_reset.htm
tech.root: seccrypto
ms.assetid: 503062c3-8a73-4218-a826-c72f926f36db
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: CEnroll object [Security],Reset method, ICEnroll3 interface [Security],Reset method, ICEnroll3.Reset, ICEnroll3::Reset, ICEnroll4 interface [Security],Reset method, ICEnroll4::Reset, Reset, Reset method [Security], Reset method [Security],CEnroll object, Reset method [Security],ICEnroll3 interface, Reset method [Security],ICEnroll4 interface, security.icenroll4_reset, xenroll/ICEnroll3::Reset, xenroll/ICEnroll4::Reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xenroll.h
req.include-header: 
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.Reset
 - ICEnroll3.Reset
 - CEnroll.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll3::Reset


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>Reset</b> method returns the 
certificate enrollment control  object to its initial <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a> and thereby allow reuse of the control. This method was first defined in the <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a> interface.


## -parameters






## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>
 

 

