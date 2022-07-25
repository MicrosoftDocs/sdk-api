---
UID: NF:cfgmgr32.CM_Enumerate_Classes
title: CM_Enumerate_Classes function (cfgmgr32.h)
description: The CM_Enumerate_Classes function, when called repeatedly, enumerates the local machine's installed device classes by supplying each class's GUID.
helpviewer_keywords: ["CM_Enumerate_Classes","CM_Enumerate_Classes function [Device and Driver Installation]","cfgmgr32/CM_Enumerate_Classes","cfgmgrfn_ab0123b7-a657-40ee-aede-e58957589d3c.xml","devinst.cm_enumerate_classes"]
old-location: devinst\cm_enumerate_classes.htm
tech.root: devinst
ms.assetid: 37e3f6fa-b207-406d-9cfa-e5f11aead821
ms.date: 12/05/2018
ms.keywords: CM_Enumerate_Classes, CM_Enumerate_Classes function [Device and Driver Installation], cfgmgr32/CM_Enumerate_Classes, cfgmgrfn_ab0123b7-a657-40ee-aede-e58957589d3c.xml, devinst.cm_enumerate_classes
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Enumerate_Classes
 - cfgmgr32/CM_Enumerate_Classes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
api_name:
 - CM_Enumerate_Classes
---

# CM_Enumerate_Classes function


## -description

The <b>CM_Enumerate_Classes</b> function, when called repeatedly, enumerates the local machine's installed <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device classes</a> by supplying each class's GUID.

## -parameters

### -param ulClassIndex [in]

Caller-supplied index into the machine's list of device classes. For more information, see the <b>Remarks</b> section.

### -param ClassGuid [out]

Caller-supplied address of a GUID structure (described in the Microsoft Windows SDK) to receive a device class's GUID.

### -param ulFlags [in]

Beginning with Windows 8, callers can specify the following flags:





#### CM_ENUMERATE_CLASSES_INSTALLER

Enumerate device setup classes.



#### CM_ENUMERATE_CLASSES_INTERFACE

Enumerate device interface classes.

Otherwise, should be set to zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

To enumerate the local machine's device classes, call <b>CM_Enumerate_Classes</b> repeatedly, starting with a <i>ulClassIndex</i> value of zero and incrementing the index value with each subsequent call until the function returns CR_NO_SUCH_VALUE. Some index values might represent list entries containing invalid class data, in which case the function returns CR_INVALID_DATA. This return value can be ignored.

The class GUIDs obtained from this function can be used as input to the <a href="/windows-hardware/drivers/install/using-device-installation-functions#ddk-update-driver-function-dg">device installation functions</a>.

Beginning with Windows 8 and later operating systems, callers can use the <b>ulFlags</b> member to specify which device classes CM_Enumerate_Classes should return. Prior to Windows 8, CM_Enumerate_Classes returned only device setup classes.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_enumerate_classes_ex">CM_Enumerate_Classes_Ex</a>