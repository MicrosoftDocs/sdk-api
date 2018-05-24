---
UID: NS:naptypes.tagNapComponentRegistrationInfo
title: tagNapComponentRegistrationInfo
author: windows-driver-content
description: Defines a registered NAP component such as a SHA, SHV, or enforcement client.
old-location: nap\napcomponentregistrationinfo_struct.htm
old-project: NAP
ms.assetid: adcc7238-d1c1-4d8c-b496-d2925bed0123
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: NapComponentRegistrationInfo, NapComponentRegistrationInfo structure [NAP], nap.napcomponentregistrationinfo_struct, naptypes/NapComponentRegistrationInfo, tagNapComponentRegistrationInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: NapComponentRegistrationInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	NapTypes.h
api_name:
-	NapComponentRegistrationInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagNapComponentRegistrationInfo structure


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>NapComponentRegistrationInfo</b> structure defines a registered NAP component such as a SHA, SHV, or enforcement client.


## -struct-fields




### -field id

A <a href="https://msdn.microsoft.com/54f2866b-4333-4fc8-bb25-b7d4ae72b7dc">NapComponentId</a> value that contains the unique identifier of the component.


### -field friendlyName

A <a href="https://msdn.microsoft.com/92261dd3-504d-4a4b-b6fa-86f4f97a0df0">CountedString</a> structure that contains the friendly (human-readable) name of the component.


### -field description

A <a href="https://msdn.microsoft.com/92261dd3-504d-4a4b-b6fa-86f4f97a0df0">CountedString</a> structure that contains a description of the component.


### -field version

A <a href="https://msdn.microsoft.com/92261dd3-504d-4a4b-b6fa-86f4f97a0df0">CountedString</a> structure that contains the version of the component.


### -field vendorName

A <a href="https://msdn.microsoft.com/92261dd3-504d-4a4b-b6fa-86f4f97a0df0">CountedString</a> structure that contains the vendor name for the component.


### -field infoClsid

The <a href="http://go.microsoft.com/fwlink/p/?linkid=113751">CLSID</a>of the COM object that implements
   the <a href="https://msdn.microsoft.com/eeff4f57-72e0-465f-9a18-ed72dad82bc7">INapComponentInfo</a> interface. This interface
   is used to retrieve more detailed and localized
   information about the NAP component.

Currently, enforcement clients do not need to
   provide a valid <i>infoClsid</i>.


### -field configClsid

The <a href="http://go.microsoft.com/fwlink/p/?linkid=113751">CLSID</a> of the COM object that implements
   the <a href="https://msdn.microsoft.com/979b5c34-8efe-4c48-8236-53fbd25d4249">INapComponentConfig</a> interface. This interface is used to launch a customized user interface and to get and set SHV configuration settings.

Currently, SHAs and enforcement clients do not need to
   provide a valid <i>configClsid</i>.


### -field registrationDate

A <a href="http://go.microsoft.com/fwlink/p/?linkid=90006">FILETIME</a> structure that contains the registration information date.


### -field componentType

A value that defines the component type.

For enforcement clients this value should be either  <a href="https://msdn.microsoft.com/2727487c-8c6a-4cd9-b6d8-253191a7d7f6">ComponentTypeEnforcementClientSoH</a> or <b>ComponentTypeEnforcementClientRp</b>.

Currently, <i>componentType</i> is ignored for SHAs and SHVs and should be set to 0x00000000.


## -remarks



This registration information is not localized, it is provided in US-English only.

When NAP components are registered through the registration APIs, the <i>registrationDate</i> field is ignored.

When information about registered NAP
   components is retrieved, if there is no valid <i>infoClsid</i>,  <i>configClsid</i>, or <i>registrationDate</i>, they are set to 0.




## -see-also




<a href="https://msdn.microsoft.com/92261dd3-504d-4a4b-b6fa-86f4f97a0df0">CountedString</a>



<a href="https://msdn.microsoft.com/eeff4f57-72e0-465f-9a18-ed72dad82bc7">INapComponentInfo</a>



<a href="https://msdn.microsoft.com/e391be3c-95ab-4c80-a5d8-8a8fef28e56b">NAP Reference</a>



<a href="https://msdn.microsoft.com/68048587-0f7e-48d4-9326-768a977ea3ee">NAP Structures</a>
 

 

