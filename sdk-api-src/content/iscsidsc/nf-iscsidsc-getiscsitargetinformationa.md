---
UID: NF:iscsidsc.GetIScsiTargetInformationA
title: GetIScsiTargetInformationA function
author: windows-sdk-content
description: GetIscsiTargetInformation function retrieves information about the specified target.
old-location: iscsidisc\getiscsitargetinformation.htm
tech.root: iSCSIDisc
ms.assetid: 3db31d0b-ed08-432b-9c28-a700c4a9d369
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetIScsiTargetInformationA, GetIscsiTargetInformation, GetIscsiTargetInformation function [iSCSI Discovery Library API], GetIscsiTargetInformationA, GetIscsiTargetInformationW, iscsidisc.getiscsitargetinformation, iscsidsc/GetIscsiTargetInformation, iscsidsc/GetIscsiTargetInformationA, iscsidsc/GetIscsiTargetInformationW
ms.topic: function
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetIscsiTargetInformationW (Unicode) and GetIscsiTargetInformationA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - GetIscsiTargetInformation
 - GetIscsiTargetInformationA
 - GetIscsiTargetInformationW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetIScsiTargetInformationA function


## -description


The <b>GetIscsiTargetInformation</b> function retrieves information about the specified target.



## -parameters




### -param TargetName [in]

The name of the target for which information is retrieved.


### -param DiscoveryMechanism [in, optional]

A text description of the mechanism that was used to discover the target (for example, "iSNS:", "SendTargets:" or "HBA:"). A value of <b>null</b> indicates that no discovery mechanism is specified.


### -param InfoClass [in]

A value of type <a href="https://msdn.microsoft.com/2ef6cff7-b5ab-463d-b274-62be81bc9295">TARGET_INFORMATION_CLASS</a> that indicates the type of information to retrieve.


### -param BufferSize [in, out]

A pointer to a location that, on input, contains the size (in bytes) of the buffer that <i>Buffer</i> points to. If the operation succeeds, the location receives the number of bytes retrieved. If the operation fails, the location receives the size of the buffer required to contain the output data. 


### -param Buffer [out]

The buffer that contains the output data. The output data consists in <b>null</b>-terminated strings, with a double <b>null</b> termination after the last string. 


## -returns



Returns ERROR_SUCCESS if successful and ERROR_INSUFFICIENT_BUFFER if the buffer size at Buffer was insufficient to contain the output data. Otherwise, <b>GetIscsiTargetInformation</b> returns the appropriate Win32 or iSCSI error code on failure.




## -remarks



The iSCSI initiator service can acquire information about a single target through multiple discovery mechanisms and initiators, and the information can be different in each case, so the iSCSI initiator service maintains a list of <i>target instances</i> which are organized according to the discovery method.

For instance, if a single target is discovered by multiple initiators, each of which uses a different target portal group to discover the target, the iSCSI initiator will create multiple target instances for the target, each of which refers to a different target portal group.

Since the information associated with a target is relative to the way in which it was discovered, the caller must specify the discovery mechanism in the <i>DiscoveryMechanism</i> parameter, using a correctly formatted string identifier for the discovery mechanism. The caller can retrieve a list of valid identifiers for discovery mechanisms by setting the <i>InfoClass</i> parameter to <b>null</b>.






## -see-also




<a href="https://msdn.microsoft.com/bdc27e67-1d64-42cd-adfa-a792012b7142">ISCSI_TARGET_MAPPING</a>



<a href="https://msdn.microsoft.com/8b7e874b-5d2b-4948-98f2-1bcd6d4f8ca6">ISCSI_TARGET_PORTAL_GROUP</a>



<a href="https://msdn.microsoft.com/1997b1d0-6723-434c-bca7-513e4dc30ee6">TARGETPROTOCOLTYPE</a>



<a href="https://msdn.microsoft.com/2ef6cff7-b5ab-463d-b274-62be81bc9295">TARGET_INFORMATION_CLASS</a>
 

 

