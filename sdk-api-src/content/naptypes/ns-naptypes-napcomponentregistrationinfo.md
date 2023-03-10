---
UID: NS:naptypes.tagNapComponentRegistrationInfo
title: NapComponentRegistrationInfo (naptypes.h)
description: Defines a registered NAP component such as a SHA, SHV, or enforcement client.
helpviewer_keywords: ["NapComponentRegistrationInfo","NapComponentRegistrationInfo structure [NAP]","nap.napcomponentregistrationinfo_struct","naptypes/NapComponentRegistrationInfo"]
old-location: nap\napcomponentregistrationinfo_struct.htm
tech.root: NAP
ms.assetid: adcc7238-d1c1-4d8c-b496-d2925bed0123
ms.date: 12/05/2018
ms.keywords: NapComponentRegistrationInfo, NapComponentRegistrationInfo structure [NAP], nap.napcomponentregistrationinfo_struct, naptypes/NapComponentRegistrationInfo
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NapComponentRegistrationInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNapComponentRegistrationInfo
 - naptypes/tagNapComponentRegistrationInfo
 - NapComponentRegistrationInfo
 - naptypes/NapComponentRegistrationInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - NapComponentRegistrationInfo
---

# NapComponentRegistrationInfo structure


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>NapComponentRegistrationInfo</b> structure defines a registered NAP component such as a SHA, SHV, or enforcement client.

## -struct-fields

### -field id

A <a href="/windows/desktop/NAP/nap-datatypes">NapComponentId</a> value that contains the unique identifier of the component.

### -field friendlyName

A <a href="/windows/desktop/api/naptypes/ns-naptypes-countedstring">CountedString</a> structure that contains the friendly (human-readable) name of the component.

### -field description

A <a href="/windows/desktop/api/naptypes/ns-naptypes-countedstring">CountedString</a> structure that contains a description of the component.

### -field version

A <a href="/windows/desktop/api/naptypes/ns-naptypes-countedstring">CountedString</a> structure that contains the version of the component.

### -field vendorName

A <a href="/windows/desktop/api/naptypes/ns-naptypes-countedstring">CountedString</a> structure that contains the vendor name for the component.

### -field infoClsid

The <a href="/windows/win32/com/clsid-key-hklm">CLSID</a> of the COM object that implements
   the <a href="/windows/desktop/NAP/inapcomponentinfo">INapComponentInfo</a> interface. This interface
   is used to retrieve more detailed and localized
   information about the NAP component.

Currently, enforcement clients do not need to
   provide a valid <i>infoClsid</i>.

### -field configClsid

The <a href="/windows/win32/com/clsid-key-hklm">CLSID</a> of the COM object that implements
   the <a href="/windows/desktop/NAP/inapcomponentconfig">INapComponentConfig</a> interface. This interface is used to launch a customized user interface and to get and set SHV configuration settings.

Currently, SHAs and enforcement clients do not need to
   provide a valid <i>configClsid</i>.

### -field registrationDate

A <a href="/windows/win32/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the registration information date.

### -field componentType

A value that defines the component type.

For enforcement clients this value should be either  <a href="/windows/desktop/NAP/nap-type-constants">ComponentTypeEnforcementClientSoH</a> or <b>ComponentTypeEnforcementClientRp</b>.

Currently, <i>componentType</i> is ignored for SHAs and SHVs and should be set to 0x00000000.

## -remarks

This registration information is not localized, it is provided in US-English only.

When NAP components are registered through the registration APIs, the <i>registrationDate</i> field is ignored.

When information about registered NAP
   components is retrieved, if there is no valid <i>infoClsid</i>,  <i>configClsid</i>, or <i>registrationDate</i>, they are set to 0.

## -see-also

<a href="/windows/desktop/api/naptypes/ns-naptypes-countedstring">CountedString</a>



<a href="/windows/desktop/NAP/inapcomponentinfo">INapComponentInfo</a>



<a href="/windows/desktop/NAP/nap-reference">NAP Reference</a>



<a href="/windows/desktop/NAP/nap-structures">NAP Structures</a>