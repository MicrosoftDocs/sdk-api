---
UID: NN:azroles.IAzPrincipalLocator
title: IAzPrincipalLocator (azroles.h)
description: Locates and chooses ADAM principals in Authorization Manager.
helpviewer_keywords: ["IAzPrincipalLocator","IAzPrincipalLocator interface [Security]","IAzPrincipalLocator interface [Security]","described","azroles/ IAzPrincipalLocator","security.iazprincipallocator"]
old-location: security\iazprincipallocator.htm
tech.root: security
ms.assetid: 7ae3f0a3-9eeb-44d9-954a-a6526bb4eb3f
ms.date: 12/05/2018
ms.keywords: IAzPrincipalLocator, IAzPrincipalLocator interface [Security], IAzPrincipalLocator interface [Security],described, azroles/ IAzPrincipalLocator, security.iazprincipallocator
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzPrincipalLocator
 - azroles/IAzPrincipalLocator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzPrincipalLocator
---

# IAzPrincipalLocator interface


## -description

The <b>IAzPrincipalLocator</b> interface locates and chooses Active Directory Application Mode (ADAM) principals in Authorization Manager.

## -remarks

An <b>IAzPrincipalLocator</b> object can contain a name resolver and an object picker. A name resolver translates <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs) into display names. An object picker displays a dialog box that enables a user to select from a list of ADAM principals. The dialog box can appear when a user modifies application groups or roles through the Authorization Manager user interface.

The <b>IAzPrincipalLocator</b> interface must be registered under the following key. <b>HKEY_LOCAL_MACHINE</b>&#92;<b>Software</b>&#92;<b>Microsoft</b>&#92;<b>AzMan</b>&#92;<b>ObjectPicker</b></p>Under this registry key, create a subkey with a value of the COM class ID of the <b>IAzPrincipalLocator</b> interface. Authorization Manager supports only one registered principal locator.