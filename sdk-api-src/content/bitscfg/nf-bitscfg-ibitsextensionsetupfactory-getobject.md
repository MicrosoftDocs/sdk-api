---
UID: NF:bitscfg.IBITSExtensionSetupFactory.GetObject
title: IBITSExtensionSetupFactory::GetObject (bitscfg.h)
description: Use the GetObject method to retrieve a pointer to the IBITSExtensionSetup interface. This method performs the same binding that the ADsGetObject ADSI function performs.
helpviewer_keywords: ["GetObject","GetObject method [BITS]","GetObject method [BITS]","IBITSExtensionSetupFactory interface","IBITSExtensionSetupFactory interface [BITS]","GetObject method","IBITSExtensionSetupFactory.GetObject","IBITSExtensionSetupFactory::GetObject","_drz_ibitsextensionsetupfactory_getobject","bits.ibitsextensionsetupfactory_getobject","bitscfg/IBITSExtensionSetupFactory::GetObject"]
old-location: bits\ibitsextensionsetupfactory_getobject.htm
tech.root: Bits
ms.assetid: ac0bb9d5-3f1f-4c9b-bd7d-905e0451bf70
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method [BITS], GetObject method [BITS],IBITSExtensionSetupFactory interface, IBITSExtensionSetupFactory interface [BITS],GetObject method, IBITSExtensionSetupFactory.GetObject, IBITSExtensionSetupFactory::GetObject, _drz_ibitsextensionsetupfactory_getobject, bits.ibitsextensionsetupfactory_getobject, bitscfg/IBITSExtensionSetupFactory::GetObject
req.header: bitscfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bitscfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: BitsMgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on  Windows XP
ms.custom: 19H1
f1_keywords:
 - IBITSExtensionSetupFactory::GetObject
 - bitscfg/IBITSExtensionSetupFactory::GetObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsMgr.dll
api_name:
 - IBITSExtensionSetupFactory.GetObject
---

# IBITSExtensionSetupFactory::GetObject


## -description

Use the 
<b>GetObject</b> method to retrieve a pointer to the 
<a href="/windows/desktop/api/bitscfg/nn-bitscfg-ibitsextensionsetup">IBITSExtensionSetup</a> interface. This method performs the same binding that the 
<a href="/windows/desktop/api/adshlp/nf-adshlp-adsgetobject">ADsGetObject</a> ADSI function performs.

## -parameters

### -param Path [in]

Null-terminated string containing the path to the directory service. For example, "IIS://&lt;machine name&gt;/w3svc/1/<i>virtual directory</i>".

### -param ppExtensionSetup [out]

Use the 
<a href="/windows/desktop/api/bitscfg/nn-bitscfg-ibitsextensionsetup">IBITSExtensionSetup</a> interface to enable and disable BITS upload for the given virtual directory.

## -returns

This method returns <b>S_OK</b> for success. Otherwise, the method failed.

## -see-also

<a href="/windows/desktop/api/bitscfg/nn-bitscfg-ibitsextensionsetup">IBITSExtensionSetup</a>