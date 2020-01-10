---
UID: NF:iscsidsc.ReportIScsiPersistentLoginsW
title: ReportIScsiPersistentLoginsW function (iscsidsc.h)
description: ReportIscsiPersistentLogins function retrieves the list of persistent login targets.
old-location: iscsidisc\reportiscsipersistentlogins.htm
tech.root: iSCSIDisc
ms.assetid: 0ab1a864-b44e-4307-9f7c-93cc0d40ff3a
ms.date: 12/05/2018
ms.keywords: ReportIScsiPersistentLoginsW, ReportIscsiPersistentLogins, ReportIscsiPersistentLogins function [iSCSI Discovery Library API], ReportIscsiPersistentLoginsA, ReportIscsiPersistentLoginsW, iscsidisc.reportiscsipersistentlogins, iscsidsc/ReportIscsiPersistentLogins, iscsidsc/ReportIscsiPersistentLoginsA, iscsidsc/ReportIscsiPersistentLoginsW
f1_keywords:
- iscsidsc/ReportIscsiPersistentLogins
dev_langs:
- c++
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReportIscsiPersistentLoginsW (Unicode) and ReportIscsiPersistentLoginsA (ANSI)
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
- ReportIscsiPersistentLogins
- ReportIscsiPersistentLoginsA
- ReportIscsiPersistentLoginsW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ReportIScsiPersistentLoginsW function


## -description


The <b>ReportIscsiPersistentLogins</b> function retrieves the list of persistent login targets.



## -parameters




### -param Count [out]

A pointer to the location that receives a count of the elements specified by  <i>PersistentLoginInfo</i>.


### -param PersistentLoginInfo [in, out]

An array of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-persistent_iscsi_login_infoa">PERSISTENT_ISCSI_LOGIN_INFO</a> structures that, on output, describe the persistent login targets.


### -param BufferSizeInBytes [in, out]

A pointer to a location that, on input, contains the byte-size of the buffer space that <i>PersistentLoginInfo</i>  specifies. If the buffer size is insufficient, this parameter specifies what is  required to contain the output data. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer specified by <i>PersistentLoginInfo</i> is insufficient to contain the output data. 

Otherwise, <b>ReportIscsiPersistentLogins</b> returns the appropriate Win32 or iSCSI error code on failure.




## -remarks



The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-persistent_iscsi_login_infoa">PERSISTENT_ISCSI_LOGIN_INFO</a> structure provides an initiator with the information required to log in to a target each time the initiator device is started.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-addpersistentiscsidevicea">AddPersistentIscsiDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-clearpersistentiscsidevices">ClearPersistentIscsiDevices</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-persistent_iscsi_login_infoa">PERSISTENT_ISCSI_LOGIN_INFO</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removeiscsipersistenttargeta">RemoveIscsiPersistentTarget</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removepersistentiscsidevicea">RemovePersistentIscsiDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportpersistentiscsidevicesa">ReportPersistentIscsiDevices</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-setuppersistentiscsidevices">SetupPersistentIscsiDevices</a>
 

 

