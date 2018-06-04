---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# CM_Enumerate_Classes_Ex function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/library/windows/hardware/ff538021">CM_Enumerate_Classes</a> instead.]

The <b>CM_Enumerate_Classes_Ex</b> function, when called repeatedly, enumerates a local or a remote machine's installed <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device classes</a>, by supplying each class's GUID.


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

Caller-supplied machine handle, obtained from a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff537948">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



To enumerate the local or a remote machine's device classes, call <b>CM_Enumerate_Classes_Ex</b> repeatedly, starting with a <i>ulClassIndex</i> index value of zero and incrementing the index value with each subsequent call until the function returns CR_NO_SUCH_VALUE. Some index values might represent list entries containing invalid class data, in which case the function returns CR_INVALID_DATA. This return value can be ignored.

The class GUIDs obtained from this function can be used as input to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff541299">device installation functions</a>.

Beginning with Windows 8 and later operating systems, callers can use the <b>ulFlags</b> member to specify which device classes CM_Enumerate_Classes_Ex should return. Prior to Windows 8, CM_Enumerate_Classes_Ex returned only device setup classes.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538021">CM_Enumerate_Classes</a>
 

 

