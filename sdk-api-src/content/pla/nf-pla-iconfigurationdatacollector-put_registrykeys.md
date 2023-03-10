---
UID: NF:pla.IConfigurationDataCollector.put_RegistryKeys
title: IConfigurationDataCollector::put_RegistryKeys (pla.h)
description: Retrieves or sets a list of registry keys to collect. (Put)
helpviewer_keywords: ["IConfigurationDataCollector interface [PLA]","RegistryKeys property","IConfigurationDataCollector.RegistryKeys","IConfigurationDataCollector.put_RegistryKeys","IConfigurationDataCollector::RegistryKeys","IConfigurationDataCollector::get_RegistryKeys","IConfigurationDataCollector::put_RegistryKeys","RegistryKeys property [PLA]","RegistryKeys property [PLA]","IConfigurationDataCollector interface","base.iconfigurationdatacollector_registrykeys","pla.iconfigurationdatacollector_registrykeys","pla/IConfigurationDataCollector::RegistryKeys","pla/IConfigurationDataCollector::get_RegistryKeys","pla/IConfigurationDataCollector::put_RegistryKeys","put_RegistryKeys"]
old-location: pla\iconfigurationdatacollector_registrykeys.htm
tech.root: PLA
ms.assetid: 990a5f92-2285-4461-8020-25028d2cab90
ms.date: 12/05/2018
ms.keywords: IConfigurationDataCollector interface [PLA],RegistryKeys property, IConfigurationDataCollector.RegistryKeys, IConfigurationDataCollector.put_RegistryKeys, IConfigurationDataCollector::RegistryKeys, IConfigurationDataCollector::get_RegistryKeys, IConfigurationDataCollector::put_RegistryKeys, RegistryKeys property [PLA], RegistryKeys property [PLA],IConfigurationDataCollector interface, base.iconfigurationdatacollector_registrykeys, pla.iconfigurationdatacollector_registrykeys, pla/IConfigurationDataCollector::RegistryKeys, pla/IConfigurationDataCollector::get_RegistryKeys, pla/IConfigurationDataCollector::put_RegistryKeys, put_RegistryKeys
req.header: pla.h
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
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConfigurationDataCollector::put_RegistryKeys
 - pla/IConfigurationDataCollector::put_RegistryKeys
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IConfigurationDataCollector.RegistryKeys
 - IConfigurationDataCollector.get_RegistryKeys
 - IConfigurationDataCollector.put_RegistryKeys
---

# IConfigurationDataCollector::put_RegistryKeys


## -description

Retrieves or sets a list of registry keys to collect.

This property is read/write.

## -parameters

## -remarks

You can collect registry data from the following registry hives:

<ul>
<li><b>HKEY_CLASSES_ROOT</b></li>
<li><b>HKEY_CURRENT_CONFIG</b></li>
<li><b>HKEY_CURRENT_USER</b></li>
<li><b>HKEY_LOCAL_MACHINE</b></li>
<li><b>HKEY_USERS</b></li>
</ul>
To collect a registry value, specify the full path to the value name, for example, `\HKEY_LOCAL_MACHINE\MyKey\MyValue`.

To collect all the values under a registry key, specify the full path to the registry key, for example, `\HKEY_LOCAL_MACHINE\MyKey\`.

To collect all the values under a registry key and its subkeys, use two backslashes for the last path delimiter, for example, `\\computername\HKEY_LOCAL_MACHINE\MyKey\\`. PLA recursively collects the registry data down to the level specified in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-iconfigurationdatacollector-get_registrymaxrecursivedepth">IConfigurationDataCollector::RegistryMaxRecursiveDepth</a> property.

To collect registry information from a remote computer, include the computer name at the beginning of the registry path, for example, `\\computername\HKEY_LOCAL_MACHINE\MyKey\MyValue`.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-iconfigurationdatacollector">IConfigurationDataCollector</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-iconfigurationdatacollector-get_registrymaxrecursivedepth">IConfigurationDataCollector::RegistryMaxRecursiveDepth</a>
