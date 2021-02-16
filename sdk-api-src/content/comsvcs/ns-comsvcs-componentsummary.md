---
UID: NS:comsvcs._ComponentSummary
title: ComponentSummary (comsvcs.h)
description: Represents summary information about a COM+ component hosted in a particular process. It can also represent a Services Without Components (SWC) context.
helpviewer_keywords: ["ComponentSummary","ComponentSummary structure [COM+]","comsvcs/ComponentSummary","cos.componentsummary"]
old-location: cos\componentsummary.htm
tech.root: cos
ms.assetid: df752c4a-6a8d-4eac-b3dc-1647bf8a8e5a
ms.date: 12/05/2018
ms.keywords: ComponentSummary, ComponentSummary structure [COM+], comsvcs/ComponentSummary, cos.componentsummary
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: ComponentSummary
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ComponentSummary
 - comsvcs/_ComponentSummary
 - ComponentSummary
 - comsvcs/ComponentSummary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - ComponentSummary
---

# ComponentSummary structure


## -description

Represents summary information about a COM+ component hosted in a particular process. It can also represent a Services Without Components (SWC) context.

## -struct-fields

### -field ApplicationInstanceId

The application instance GUID that uniquely identifies the process that hosts the component.

### -field PartitionId

The partition ID of the component.

### -field ApplicationId

The application ID of the component. The special value {84ac4168-6fe5-4308-a2ed-03688a023c7a} indicates that this is an SWC context.

### -field Clsid

The CLSID of the component.

### -field ClassName

The name of the component. Usually, this is the component's ProgID (or the string representation of the component's CLSID if the component does not have a ProgID). For SWC contexts, this is the context name property configured for the context. Space for this string is allocated by the method called and freed by the caller (for more information, see <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>). This member is not returned by default. To return this member, specify the GATD_INCLUDE_CLASS_NAME flag when you call a method that returns a <b>ComponentSummary</b> structure.

### -field ApplicationName

The name of the COM+ application, or the application name property configured for an SWC context. Space for this string is allocated by the method called and freed by the caller (for more information, see <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>). This member is not returned by default. To return this member, specify the GATD_INCLUDE_APPLICATION_NAME flag when you call a method that returns a <b>ComponentSummary</b> structure.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a>