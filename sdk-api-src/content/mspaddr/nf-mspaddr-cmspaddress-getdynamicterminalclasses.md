---
UID: NF:mspaddr.CMSPAddress.GetDynamicTerminalClasses
title: CMSPAddress::GetDynamicTerminalClasses (mspaddr.h)
description: The GetDynamicTerminalClasses method is called by our wrapper methods to get an array of dynamic terminal classes that can be used on this address.
helpviewer_keywords: ["CMSPAddress interface [TAPI 2.2]","GetDynamicTerminalClasses method","CMSPAddress.GetDynamicTerminalClasses","CMSPAddress::GetDynamicTerminalClasses","GetDynamicTerminalClasses","GetDynamicTerminalClasses method [TAPI 2.2]","GetDynamicTerminalClasses method [TAPI 2.2]","CMSPAddress interface","_tapi3_cmspaddress_getdynamicterminalclasses","mspaddr/CMSPAddress::GetDynamicTerminalClasses","tapi3.cmspaddress_getdynamicterminalclasses"]
old-location: tapi3\cmspaddress_getdynamicterminalclasses.htm
tech.root: tapi3
ms.assetid: 62ded118-ee43-4500-97e2-4177518465a6
ms.date: 12/05/2018
ms.keywords: CMSPAddress interface [TAPI 2.2],GetDynamicTerminalClasses method, CMSPAddress.GetDynamicTerminalClasses, CMSPAddress::GetDynamicTerminalClasses, GetDynamicTerminalClasses, GetDynamicTerminalClasses method [TAPI 2.2], GetDynamicTerminalClasses method [TAPI 2.2],CMSPAddress interface, _tapi3_cmspaddress_getdynamicterminalclasses, mspaddr/CMSPAddress::GetDynamicTerminalClasses, tapi3.cmspaddress_getdynamicterminalclasses
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CMSPAddress::GetDynamicTerminalClasses
 - mspaddr/CMSPAddress::GetDynamicTerminalClasses
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspaddr.h
api_name:
 - CMSPAddress.GetDynamicTerminalClasses
---

# CMSPAddress::GetDynamicTerminalClasses


## -description

The 
<b>GetDynamicTerminalClasses</b> method is called by our wrapper methods to get an array of dynamic terminal classes that can be used on this address. The semantics of the arguments are the same as for 
<a href="/windows/desktop/api/mspaddr/nf-mspaddr-cmspaddress-getstaticterminals">GetStaticTerminals</a>. This method simply asks the Terminal Manager for the terminal classes. MSPs that implement additional, custom types of dynamic terminals, or that want to disallow the use of certain dynamic terminal classes from the Terminal Manager, would want to override this method.

## -parameters

### -param pdwNumClasses [out]

Pointer to number of dynamic terminals.

### -param pTerminalClasses [out]

Pointer to array of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interfaces.

## -see-also

<a href="/windows/desktop/api/mspaddr/nl-mspaddr-cmspaddress">CMSPAddress</a>