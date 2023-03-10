---
UID: NN:fhcfg.IFhReassociation
title: IFhReassociation (fhcfg.h)
description: This interface allows client applications to reassociate a File History configuration from a File History target with the current user.
helpviewer_keywords: ["IFhReassociation","IFhReassociation interface [Windows API]","IFhReassociation interface [Windows API]","described","fhcfg/IFhReassociation","winprog.ifhreassociation"]
old-location: winprog\ifhreassociation.htm
tech.root: winprog
ms.assetid: B1CBD7DD-5B4D-4B3E-BE7D-B6497ABFB588
ms.date: 12/05/2018
ms.keywords: IFhReassociation, IFhReassociation interface [Windows API], IFhReassociation interface [Windows API],described, fhcfg/IFhReassociation, winprog.ifhreassociation
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
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
 - IFhReassociation
 - fhcfg/IFhReassociation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhReassociation
---

# IFhReassociation interface


## -description

This interface allows client applications to reassociate a File History configuration from a File History target with the current user. Reassociation serves two purposes:<ul>
<li>It allows the user to access the data that was backed up to the target in the past, possibly from a different computer or under a different account.</li>
<li>It allows the user to continue to back up data to the target, possibly on a new computer or under a new account name.</li>
</ul>

> [!NOTE] 
> **IFhReassociation** is deprecated and may be altered or unavailable in future releases.

## -inheritance

The <b>IFhReassociation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFhReassociation</b> also has these types of members:

