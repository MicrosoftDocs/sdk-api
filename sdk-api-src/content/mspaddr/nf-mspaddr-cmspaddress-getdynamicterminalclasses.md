---
UID: NF:mspaddr.CMSPAddress.GetDynamicTerminalClasses
title: CMSPAddress::GetDynamicTerminalClasses
author: windows-sdk-content
description: The GetDynamicTerminalClasses method is called by our wrapper methods to get an array of dynamic terminal classes that can be used on this address.
old-location: tapi3\cmspaddress_getdynamicterminalclasses.htm
tech.root: tapi
ms.assetid: 62ded118-ee43-4500-97e2-4177518465a6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CMSPAddress interface [TAPI 2.2],GetDynamicTerminalClasses method, CMSPAddress.GetDynamicTerminalClasses, CMSPAddress::GetDynamicTerminalClasses, GetDynamicTerminalClasses, GetDynamicTerminalClasses method [TAPI 2.2], GetDynamicTerminalClasses method [TAPI 2.2],CMSPAddress interface, _tapi3_cmspaddress_getdynamicterminalclasses, mspaddr/CMSPAddress::GetDynamicTerminalClasses, tapi3.cmspaddress_getdynamicterminalclasses
ms.topic: method
req.header: mspaddr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspaddr.h
api_name:
 - CMSPAddress.GetDynamicTerminalClasses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMSPAddress::GetDynamicTerminalClasses


## -description


The 
<b>GetDynamicTerminalClasses</b> method is called by our wrapper methods to get an array of dynamic terminal classes that can be used on this address. The semantics of the arguments are the same as for 
<a href="https://msdn.microsoft.com/en-us/library/ms726432(v=VS.85).aspx">GetStaticTerminals</a>. This method simply asks the Terminal Manager for the terminal classes. MSPs that implement additional, custom types of dynamic terminals, or that want to disallow the use of certain dynamic terminal classes from the Terminal Manager, would want to override this method.


## -parameters




### -param pdwNumClasses [out]

Pointer to number of dynamic terminals.


### -param pTerminalClasses [out]

Pointer to array of 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interfaces.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms726419(v=VS.85).aspx">CMSPAddress</a>
 

 

