---
UID: NN:shdeprecated.IBrowserService
title: IBrowserService (shdeprecated.h)
description: Deprecated. (IBrowserService)
helpviewer_keywords: ["IBrowserService","IBrowserService interface [Windows Shell]","IBrowserService interface [Windows Shell]","described","shdeprecated/IBrowserService","shell.IBrowserService","zone_IBrowserService"]
old-location: shell\IBrowserService.htm
tech.root: shell
ms.assetid: e12ada84-0825-4946-8075-731dfc51ef50
ms.date: 12/05/2018
ms.keywords: IBrowserService, IBrowserService interface [Windows Shell], IBrowserService interface [Windows Shell],described, shdeprecated/IBrowserService, shell.IBrowserService, zone_IBrowserService
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService
 - shdeprecated/IBrowserService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService
---

# IBrowserService interface


## -description

Deprecated. The methods exposed by this interface are analogous to virtual protected methods in normal C++ inheritance. The objects' inheritance hierarchy spans multiple DLLs. The hierarchy is made up of a base class and several derived classes that correspond to controls, including CLSID_WebBrowser and the user's desktop. Objects not in the hierarchy should not implement this interface or use most of its methods.

## -inheritance

The <b>IBrowserService</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBrowserService</b> also has these types of members:

## -remarks

In a direct inheritance scheme, these methods would be protected members. For that reason, it is recommended that this interface not be used directly by implementers. If it is used directly, existing data could be at risk.
