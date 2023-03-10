---
UID: NF:cfgmgr32.CM_Enumerate_Classes_Ex
title: CM_Enumerate_Classes_Ex function (cfgmgr32.h)
description: The CM_Enumerate_Classes_Ex function, when called repeatedly, enumerates a local or a remote machine's installed device classes, by supplying each class's GUID.
helpviewer_keywords: ["CM_Enumerate_Classes_Ex","CM_Enumerate_Classes_Ex function [Device and Driver Installation]","cfgmgr32/CM_Enumerate_Classes_Ex","cfgmgrfn_586eceae-046e-4e4a-8763-e287b039585e.xml","devinst.cm_enumerate_classes_ex"]
old-location: devinst\cm_enumerate_classes_ex.htm
tech.root: devinst
ms.assetid: 8dce071c-3f91-42c2-a334-ec1051b6436a
ms.date: 12/05/2018
ms.keywords: CM_Enumerate_Classes_Ex, CM_Enumerate_Classes_Ex function [Device and Driver Installation], cfgmgr32/CM_Enumerate_Classes_Ex, cfgmgrfn_586eceae-046e-4e4a-8763-e287b039585e.xml, devinst.cm_enumerate_classes_ex
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
 - CM_Enumerate_Classes_Ex
 - cfgmgr32/CM_Enumerate_Classes_Ex
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
 - CM_Enumerate_Classes_Ex
---

# CM_Enumerate_Classes_Ex function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_enumerate_classes">CM_Enumerate_Classes</a> instead.]

The <b>CM_Enumerate_Classes_Ex</b> function, when called repeatedly, enumerates a local or a remote machine's installed <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device classes</a>, by supplying each class's GUID.

## -parameters

### -param ulClassIndex [in]

Caller-supplied index into the machine's list of device classes. For more information, see the following <b>Remarks</b> section.

### -param ClassGuid [out]

Caller-supplied address of a GUID structure (described in the Microsoft Windows SDK) to receive a device class's GUID.

### -param ulFlags [in]

Beginning with Windows 8, callers can specify the following flags:





#### CM_ENUMERATE_CLASSES_INSTALLER

Enumerate device setup classes.



#### CM_ENUMERATE_CLASSES_INTERFACE

Enumerate device interface classes.

Otherwise, should be set to zero.

### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

To enumerate the local or a remote machine's device classes, call <b>CM_Enumerate_Classes_Ex</b> repeatedly, starting with a <i>ulClassIndex</i> index value of zero and incrementing the index value with each subsequent call until the function returns CR_NO_SUCH_VALUE. Some index values might represent list entries containing invalid class data, in which case the function returns CR_INVALID_DATA. This return value can be ignored.

The class GUIDs obtained from this function can be used as input to the <a href="/windows-hardware/drivers/install/using-device-installation-functions#ddk-update-driver-function-dg">device installation functions</a>.

Beginning with Windows 8 and later operating systems, callers can use the <b>ulFlags</b> member to specify which device classes CM_Enumerate_Classes_Ex should return. Prior to Windows 8, CM_Enumerate_Classes_Ex returned only device setup classes.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_enumerate_classes">CM_Enumerate_Classes</a>