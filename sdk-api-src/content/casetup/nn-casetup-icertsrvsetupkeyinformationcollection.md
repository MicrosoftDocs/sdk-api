---
UID: NN:casetup.ICertSrvSetupKeyInformationCollection
title: ICertSrvSetupKeyInformationCollection (casetup.h)
description: Defines functionality to populate and enumerate a collection of ICertSrvSetupKeyInformation objects.
helpviewer_keywords: ["ICertSrvSetupKeyInformationCollection","ICertSrvSetupKeyInformationCollection interface [Security]","ICertSrvSetupKeyInformationCollection interface [Security]","described","casetup/ICertSrvSetupKeyInformationCollection","security.icertsrvsetupkeyinformationcollection"]
old-location: security\icertsrvsetupkeyinformationcollection.htm
tech.root: security
ms.assetid: d029dd5f-9c19-46fd-aac3-275c624a157b
ms.date: 12/05/2018
ms.keywords: ICertSrvSetupKeyInformationCollection, ICertSrvSetupKeyInformationCollection interface [Security], ICertSrvSetupKeyInformationCollection interface [Security],described, casetup/ICertSrvSetupKeyInformationCollection, security.icertsrvsetupkeyinformationcollection
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertSrvSetupKeyInformationCollection
 - casetup/ICertSrvSetupKeyInformationCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetupKeyInformationCollection
---

# ICertSrvSetupKeyInformationCollection interface


## -description

The <b>ICertSrvSetupKeyInformationCollection</b> interface defines functionality to populate and enumerate a collection of <a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetupkeyinformation">ICertSrvSetupKeyInformation</a> objects. Microsoft provides an implementation of this interface in the <b>CCertSrvSetupKeyInformationCollection</b> class. You cannot create an external instance of this interface. You obtain this interface by calling the <a href="/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-getexistingcacertificates">GetExistingCACertificates</a> method.

## -inheritance

The <b>ICertSrvSetupKeyInformationCollection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICertSrvSetupKeyInformationCollection</b> also has these types of members:

