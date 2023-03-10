---
UID: NN:iads.IDirectorySearch
title: IDirectorySearch (iads.h)
description: The IDirectorySearch interface is a pure COM interface that provides a low overhead method that non-Automation clients can use to perform queries in the underlying directory.
helpviewer_keywords: ["IDirectorySearch","IDirectorySearch interface [ADSI]","IDirectorySearch interface [ADSI]","described","_ds_idirectorysearch","adsi.idirectorysearch","iads/IDirectorySearch"]
old-location: adsi\idirectorysearch.htm
tech.root: adsi
ms.assetid: e8989795-8f72-476a-a69e-c0e8800289ab
ms.date: 12/05/2018
ms.keywords: IDirectorySearch, IDirectorySearch interface [ADSI], IDirectorySearch interface [ADSI],described, _ds_idirectorysearch, adsi.idirectorysearch, iads/IDirectorySearch
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll; Adsldp.dll; Adsldpc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectorySearch
 - iads/IDirectorySearch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
 - Adsldp.dll
 - Adsldpc.dll
api_name:
 - IDirectorySearch
---

# IDirectorySearch interface


## -description

The <b>IDirectorySearch</b> interface is a pure COM interface that provides a low overhead method that non-Automation clients can use to perform queries in the underlying directory.

Of the ADSI system-supplied providers, only the LDAP provider supports this interface.

## -inheritance

The <b>IDirectorySearch</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectorySearch</b> also has these types of members:

