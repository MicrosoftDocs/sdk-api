---
UID: NS:winbio._WINBIO_ASYNC_RESULT
title: WINBIO_ASYNC_RESULT (winbio.h)
description: Contains the results of an asynchronous operation.
helpviewer_keywords: ["*PWINBIO_ASYNC_RESULT","PWINBIO_ASYNC_RESULT","PWINBIO_ASYNC_RESULT structure pointer [Windows Biometric Framework API]","WINBIO_ASYNC_RESULT","WINBIO_ASYNC_RESULT structure [Windows Biometric Framework API]","secbiomet.winbio_async_result","winbio/PWINBIO_ASYNC_RESULT","winbio/WINBIO_ASYNC_RESULT"]
old-location: secbiomet\winbio_async_result.htm
tech.root: SecBioMet
ms.assetid: 1C8A4557-3851-4AB2-BB9B-AE199EB9D024
ms.date: 12/05/2018
ms.keywords: '*PWINBIO_ASYNC_RESULT, PWINBIO_ASYNC_RESULT, PWINBIO_ASYNC_RESULT structure pointer [Windows Biometric Framework API], WINBIO_ASYNC_RESULT, WINBIO_ASYNC_RESULT structure [Windows Biometric Framework API], secbiomet.winbio_async_result, winbio/PWINBIO_ASYNC_RESULT, winbio/WINBIO_ASYNC_RESULT'
req.header: winbio.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINBIO_ASYNC_RESULT
 - winbio/_WINBIO_ASYNC_RESULT
 - PWINBIO_ASYNC_RESULT
 - winbio/PWINBIO_ASYNC_RESULT
 - WINBIO_ASYNC_RESULT
 - winbio/WINBIO_ASYNC_RESULT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbio.h
api_name:
 - WINBIO_ASYNC_RESULT
---

# WINBIO_ASYNC_RESULT structure


## -description

The <b>WINBIO_ASYNC_RESULT</b> structure contains the results of an asynchronous operation.

## -struct-fields

### -field SessionHandle

Handle of an asynchronous session started by calling the <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a> function or the <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopenframework">WinBioAsyncOpenFramework</a> function.

### -field Operation

Type of the asynchronous operation. For more information, see <a href="/windows/desktop/SecBioMet/winbio-operation-type-constants">WINBIO_OPERATION_TYPE Constants</a>.

### -field SequenceNumber

Sequence number of the asynchronous operation. The integers are assigned sequentially for each operation in a biometric session, starting at one (1). For any session, the open operation is always assigned the first sequence number and the close operation is assigned the last sequence number. If your application queues multiple operations, you can use sequence numbers to perform error handling. For example, you can ignore operation results until a specific sequence number is sent to the application.

### -field TimeStamp

System date and time at which the biometric operation began. For more information, see the <b>GetSystemTimeAsFileTime</b> function.

### -field ApiStatus

Error code returned by the operation.

### -field UnitId

The numeric unit identifier of the biometric unit that performed the operation.

### -field UserData

Address of an optional buffer supplied by the caller. The buffer is not modified by the framework or the biometric unit. Your application can use the data to help it determine what actions to perform upon receipt of the completion notice or to maintain additional information about the requested operation.

### -field Parameters

Union that encloses nested structures that contain additional information about the success or failure of asynchronous operations begun by the client application.

### -field Parameters.Verify

Contains the results of an asynchronous call to <a href="/windows/desktop/api/winbio/nf-winbio-winbioverify">WinBioVerify</a>.

### -field Parameters.Verify.Match

Specifies whether the captured sample matched the user identity.

### -field Parameters.Verify.RejectDetail

Additional information about verification failure. For more information, see Remarks.

### -field Parameters.Identify

Contains the results of an asynchronous call to <a href="/windows/desktop/api/winbio/nf-winbio-winbioidentify">WinBioIdentify</a>.

### -field Parameters.Identify.Identity

GUID or SID of the user providing the biometric sample.

### -field Parameters.Identify.SubFactor

Sub-factor associated with the biometric sample. For more information, see Remarks.

### -field Parameters.Identify.RejectDetail

Additional information about the failure, if any, to capture and identify a biometric sample. For more information, see Remarks.

### -field Parameters.EnrollBegin

Contains the results of an asynchronous call to <a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollbegin">WinBioEnrollBegin</a>.

### -field Parameters.EnrollBegin.SubFactor

Additional information about the enrollment. For more information, see Remarks.

### -field Parameters.EnrollCapture

Contains the results of an asynchronous call to  <a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollcapture">WinBioEnrollCapture</a>.

### -field Parameters.EnrollCapture.RejectDetail

Additional information about the failure to capture a biometric sample. For more information,  see Remarks.

### -field Parameters.EnrollCommit

Contains the results of an asynchronous call to  <a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollcommit">WinBioEnrollCommit</a>.

### -field Parameters.EnrollCommit.Identity

GUID or SID of the template to be saved.

### -field Parameters.EnrollCommit.IsNewTemplate

Specifies whether the template being added to the database is new.

### -field Parameters.EnumEnrollments

Contains the results of an asynchronous call to <a href="/windows/desktop/api/winbio/nf-winbio-winbioenumenrollments">WinBioEnumEnrollments</a>.

### -field Parameters.EnumEnrollments.Identity

GUID or SID of the template from which the sub-factors were retrieved.

### -field Parameters.EnumEnrollments.SubFactorCount

Number of elements in the array pointed to by the <b>SubFactorArray</b> member.

### -field Parameters.EnumEnrollments.SubFactorArray

Pointer to an array of sub-factors. For more information, see Remarks.

### -field Parameters.CaptureSample

Contains the results of an asynchronous call to <a href="/windows/desktop/api/winbio/nf-winbio-winbiocapturesample">WinBioCaptureSample</a>.

### -field Parameters.CaptureSample.Sample

Pointer to a <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure that contains the sample.

### -field Parameters.CaptureSample.SampleSize

Size, in bytes, of the <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure returned in the <b>Sample</b> member.

### -field Parameters.CaptureSample.RejectDetail

Additional information about the failure to capture a biometric sample. For more information, see Remarks.

### -field Parameters.DeleteTemplate

Contains the results of an asynchronous call to <a href="/windows/desktop/api/winbio/nf-winbio-winbiodeletetemplate">WinBioDeleteTemplate</a>.

### -field Parameters.DeleteTemplate.Identity

GUID or SID of the template that was deleted.

### -field Parameters.DeleteTemplate.SubFactor

Additional information about the template.

### -field Parameters.GetProperty

Contains the results of an asynchronous call to <a href="/windows/desktop/api/winbio/nf-winbio-winbiogetproperty">WinBioGetProperty</a>.

### -field Parameters.GetProperty.PropertyType

Source of the property information. Currently this will be <b>WINBIO_PROPERTY_TYPE_UNIT</b>.

### -field Parameters.GetProperty.PropertyId

The property that was queried. Currently this will be <b>WINBIO_PROPERTY_SAMPLE_HINT</b>.

### -field Parameters.GetProperty.Identity

This is a reserved value and will be <b>NULL</b>.

### -field Parameters.GetProperty.SubFactor

This is reserved and will be <b>WINBIO_SUBTYPE_NO_INFORMATION</b>.

### -field Parameters.GetProperty.PropertyBufferSize

Size, in bytes, of the property value pointed to by the <b>PropertyBuffer</b> member.

### -field Parameters.GetProperty.PropertyBuffer

Pointer to  the property value.

### -field Parameters.SetProperty

Contains the results of an asynchronous call to <a href="/windows/desktop/api/winbio/nf-winbio-winbiosetproperty">WinBioSetProperty</a>. This member is supported starting in Windows 10.



##### SetProperty.PropretyBufferSize

The size, in bytes, of the structure to which the <i>PropertyBuffer</i> parameter points.

### -field Parameters.SetProperty.PropertyType

A <b>WINBIO_PROPERTY_TYPE</b> value that specifies the type of the property that was set. Currently this can only be <b>WINBIO_PROPERTY_TYPE_ACCOUNT</b>.

### -field Parameters.SetProperty.PropertyId

A <b>WINBIO_PROPERTY_ID</b> value that specifies the property that was set. Currently this value can only be <b>WINBIO_PROPERTY_ANTI_SPOOF_POLICY</b>. All other properties are read-only.

### -field Parameters.SetProperty.Identity

A <a href="/windows/desktop/SecBioMet/winbio-identity">WINBIO_IDENTITY</a> structure that specifies the account for which the property was set.

### -field Parameters.SetProperty.SubFactor

Reserved. Currently, this value will always be <b>WINBIO_SUBTYPE_NO_INFORMATION</b>.

### -field Parameters.SetProperty.PropertyBufferSize

### -field Parameters.SetProperty.PropertyBuffer

A pointer to a structure that specifies the value to which the property was set.  For the <b>WINBIO_PROPERTY_ANTI_SPOOF_POLICY</b> property, the structure is  a <a href="/windows/desktop/SecBioMet/winbio-anti-spoof-policy">WINBIO_ANTI_SPOOF_POLICY</a> structure.

### -field Parameters.GetEvent

Contains status information about the event that was raised.

### -field Parameters.GetEvent.Event

Contains event information.

### -field Parameters.ControlUnit

Contains the results of an asynchronous call to <a href="/windows/desktop/api/winbio/nf-winbio-winbiocontrolunit">WinBioControlUnit</a> or <a href="/windows/desktop/api/winbio/nf-winbio-winbiocontrolunitprivileged">WinBioControlUnitPrivileged</a>.

### -field Parameters.ControlUnit.Component

The component within the biometric unit that performed the operation.

### -field Parameters.ControlUnit.ControlCode

Vendor-defined code recognized by the biometric unit specified by the <i>UnitId</i> parameter of the <a href="/windows/desktop/api/winbio/nf-winbio-winbiocontrolunit">WinBioControlUnit</a> or  <a href="/windows/desktop/api/winbio/nf-winbio-winbiocontrolunitprivileged">WinBioControlUnitPrivileged</a> function and the adapter specified by the <i>Component</i> parameter.

### -field Parameters.ControlUnit.OperationStatus

Vendor-defined status code that specifies the outcome of the control operation.

### -field Parameters.ControlUnit.SendBuffer

Pointer to a buffer that contains the control information sent to the adapter by the component. The format and content of the buffer is vendor-defined.

### -field Parameters.ControlUnit.SendBufferSize

Size, in bytes, of the buffer specified by the <b>SendBuffer</b> member.

### -field Parameters.ControlUnit.ReceiveBuffer

Pointer to a buffer that receives information sent by the adapter specified by the  <b>Component</b> member. The format and content of the buffer is vendor-defined.

### -field Parameters.ControlUnit.ReceiveBufferSize

Size, in bytes, of the buffer specified by the <b>ReceiveBuffer</b> member.

### -field Parameters.ControlUnit.ReceiveDataSize

Size, in bytes, of the data written to the buffer specified by the <b>ReceiveBuffer</b> member.

### -field Parameters.EnumServiceProviders

Contains the results of an asynchronous call to <a href="/windows/desktop/api/winbio/nf-winbio-winbioenumserviceproviders">WinBioEnumServiceProviders</a> or <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncenumserviceproviders">WinBioAsyncEnumServiceProviders</a>.

### -field Parameters.EnumServiceProviders.BspCount

The number of structures pointed to by the <b>BspSchemaArray</b> member.

### -field Parameters.EnumServiceProviders.BspSchemaArray

Pointer to an array of <a href="/windows/desktop/SecBioMet/winbio-bsp-schema">WINBIO_BSP_SCHEMA</a> structures that contain information about each of the available service providers.

### -field Parameters.EnumBiometricUnits

Contains the results of an asynchronous call to <a href="/windows/desktop/api/winbio/nf-winbio-winbioenumbiometricunits">WinBioEnumBiometricUnits</a> or <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncenumbiometricunits">WinBioAsyncEnumBiometricUnits</a>.

### -field Parameters.EnumBiometricUnits.UnitCount

Number of structures pointed to by the <b>UnitSchemaArray</b> member.

### -field Parameters.EnumBiometricUnits.UnitSchemaArray

An array of <a href="/windows/desktop/SecBioMet/winbio-unit-schema">WINBIO_UNIT_SCHEMA</a> structures that contain information about each enumerated biometric unit.

### -field Parameters.EnumDatabases

Contains the results of an asynchronous call to <a href="/windows/desktop/api/winbio/nf-winbio-winbioenumdatabases">WinBioEnumDatabases</a> or <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncenumdatabases">WinBioAsyncEnumDatabases</a>.

### -field Parameters.EnumDatabases.StorageCount

Number of structures pointed to by the <b>StorageSchemaArray</b> member.

### -field Parameters.EnumDatabases.StorageSchemaArray

Array of <a href="/windows/desktop/SecBioMet/winbio-storage-schema">WINBIO_STORAGE_SCHEMA</a> structures that contain information about each database.

### -field Parameters.VerifyAndReleaseTicket

Reserved. This member is supported starting in Windows 10.

### -field Parameters.VerifyAndReleaseTicket.Match

Reserved.

### -field Parameters.VerifyAndReleaseTicket.RejectDetail

Reserved.

### -field Parameters.VerifyAndReleaseTicket.Ticket

Reserved.

### -field Parameters.IdentifyAndReleaseTicket

Reserved. This member is supported starting in Windows 10.

### -field Parameters.IdentifyAndReleaseTicket.Identity

Reserved.

### -field Parameters.IdentifyAndReleaseTicket.SubFactor

Reserved.

### -field Parameters.IdentifyAndReleaseTicket.RejectDetail

Reserved.

### -field Parameters.IdentifyAndReleaseTicket.Ticket

Reserved.

### -field Parameters.EnrollSelect

Contains the results of an asynchronous call to <a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollselect">WinBioEnrollSelect</a>. This member is supported starting in Windows 10.

### -field Parameters.EnrollSelect.SelectorValue

A value that identifies that individual that was  selected for enrollment.

### -field Parameters.MonitorPresence

Contains the results of an asynchronous call to <a href="/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence">WinBioMonitorPresence</a>. This member is supported starting in Windows 10.

### -field Parameters.MonitorPresence.ChangeType

A <b>WINBIO_PRESENCE_CHANGE</b> value that indicates the type of event that occurred.

### -field Parameters.MonitorPresence.PresenceCount

The size of the array that the <b>MonitorPresence.PresenceArray</b> member points to.

### -field Parameters.MonitorPresence.PresenceArray

Address of the array of <a href="/windows/desktop/SecBioMet/winbio-presence">WINBIO_PRESENCE</a> structures, one for each individual monitored.

### -field Parameters.GetProtectionPolicy

### -field Parameters.GetProtectionPolicy.Identity

### -field Parameters.GetProtectionPolicy.Policy

### -field Parameters.NotifyUnitStatusChange

### -field Parameters.NotifyUnitStatusChange.ExtendedStatus

## -remarks

Asynchronous operations are begun by opening a biometric session  or a framework session. Call <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a> to open a biometric session. Call <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopenframework">WinBioAsyncOpenFramework</a> to open a framework session.

You can use an asynchronous biometric session handle to call any of the following operations asynchronously:<ul>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiocancel">WinBioCancel</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiocapturesample">WinBioCaptureSample</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioclosesession">WinBioCloseSession</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiocontrolunit">WinBioControlUnit</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiocontrolunitprivileged">WinBioControlUnitPrivileged</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiodeletetemplate">WinBioDeleteTemplate</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollbegin">WinBioEnrollBegin</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollcapture">WinBioEnrollCapture</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollcommit">WinBioEnrollCommit</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenrolldiscard">WinBioEnrollDiscard</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumenrollments">WinBioEnumEnrollments</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiogetproperty">WinBioGetProperty</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioidentify">WinBioIdentify</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiolocatesensor">WinBioLocateSensor</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiolockunit">WinBioLockUnit</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiologonidentifieduser">WinBioLogonIdentifiedUser</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioregistereventmonitor">WinBioRegisterEventMonitor</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiounlockunit">WinBioUnlockUnit</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiounregistereventmonitor">WinBioUnregisterEventMonitor</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioverify">WinBioVerify</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiowait">WinBioWait</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiosetproperty">WinBioSetProperty</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollselect">WinBioEnrollSelect</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence">WinBioMonitorPresence</a>
</li>
</ul>


You can use an asynchronous framework handle to call the following operations asynchronously:<ul>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncenumbiometricunits">WinBioAsyncEnumBiometricUnits</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncenumdatabases">WinBioAsyncEnumDatabases</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopenframework">WinBioAsyncOpenFramework</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncenumserviceproviders">WinBioAsyncEnumServiceProviders</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncmonitorframeworkchanges">WinBioAsyncMonitorFrameworkChanges</a>
</li>
</ul>


The <b>WINBIO_ASYNC_RESULT</b> structure is allocated internally by the Windows Biometric Framework. Therefore, when you are through using it, call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the allocated memory and avoid leaks. Because this also releases all nested data structures, you should not keep a copy of any pointers returned in the <b>WINBIO_ASYNC_RESULT</b> structure. If you want to save any data returned in a nested structure, make a private copy of that data before calling <b>WinBioFree</b>.

<b>Windows 8, Windows Server 2012, Windows 8.1 and Windows Server 2012 R2:  </b>The Windows Biometric Framework supports only fingerprint readers. Therefore, if an operation fails and returns additional information in a <b>WINBIO_REJECT_DETAIL</b> constant, it will be one of the following values:<ul>
<li>WINBIO_FP_TOO_HIGH</li>
<li>WINBIO_FP_TOO_LOW</li>
<li>WINBIO_FP_TOO_LEFT</li>
<li>WINBIO_FP_TOO_RIGHT</li>
<li>WINBIO_FP_TOO_FAST</li>
<li>WINBIO_FP_TOO_SLOW</li>
<li>WINBIO_FP_POOR_QUALITY</li>
<li>WINBIO_FP_TOO_SKEWED</li>
<li>WINBIO_FP_TOO_SHORT</li>
<li>WINBIO_FP_MERGE_FAILURE</li>
</ul>


Further, if an operation uses a <b>WINBIO_BIOMETRIC_SUBTYPE</b> data type, it will be one of the following values:<ul>
<li>WINBIO_ANSI_381_POS_UNKNOWN</li>
<li>WINBIO_ANSI_381_POS_RH_THUMB</li>
<li>WINBIO_ANSI_381_POS_RH_INDEX_FINGER</li>
<li>WINBIO_ANSI_381_POS_RH_MIDDLE_FINGER</li>
<li>WINBIO_ANSI_381_POS_RH_RING_FINGER</li>
<li>WINBIO_ANSI_381_POS_RH_LITTLE_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_THUMB</li>
<li>WINBIO_ANSI_381_POS_LH_INDEX_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_MIDDLE_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_RING_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_LITTLE_FINGER</li>
<li>WINBIO_ANSI_381_POS_RH_FOUR_FINGERS</li>
<li>WINBIO_ANSI_381_POS_LH_FOUR_FINGERS</li>
<li>WINBIO_ANSI_381_POS_TWO_THUMBS</li>
</ul>

## -see-also

<a href="/windows/desktop/SecBioMet/winbio-reject-detail-constants">WINBIO_REJECT_DETAIL Constants</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopenframework">WinBioAsyncOpenFramework</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>