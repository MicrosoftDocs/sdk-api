---
UID: NC:winbio.PWINBIO_LOCATE_SENSOR_CALLBACK
title: PWINBIO_LOCATE_SENSOR_CALLBACK
author: windows-sdk-content
description: Returns results from the asynchronous WinBioLocateSensorWithCallback function.
old-location: secbiomet\pwinbio_locate_sensor_callback.htm
old-project: SecBioMet
ms.assetid: 2959B5C0-A513-4124-8391-E05E9F43CD53
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PWINBIO_LOCATE_SENSOR_CALLBACK, PWINBIO_LOCATE_SENSOR_CALLBACK callback, PWINBIO_LOCATE_SENSOR_CALLBACK callback function [Windows Biometric Framework API], secbiomet.pwinbio_locate_sensor_callback, winbio/PWINBIO_LOCATE_SENSOR_CALLBACK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winbio.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WIN32_STREAM_ID, *LPWIN32_STREAM_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio.h
api_name:
 - PWINBIO_LOCATE_SENSOR_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PWINBIO_LOCATE_SENSOR_CALLBACK callback function


## -description


Called by the Windows Biometric Framework to return results from the   asynchronous  <a href="https://msdn.microsoft.com/d94db51b-67da-477a-82e6-c92da756f017">WinBioLocateSensorWithCallback</a> function. The client application must implement this function.


<div class="alert"><b>Important</b>  We recommend that, beginning with Windows 8, you no longer use the <b>PWINBIO_LOCATE_SENSOR_CALLBACK</b>/<b>WinBioLocateSensorWithCallback</b> combination. Instead, do the following:<ul>
<li>Implement a <a href="https://msdn.microsoft.com/550EA13D-18CE-4B73-9C9B-4D5C46C48A75">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function to receive notice when the operation completes.</li>
<li>Call the <a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a> function. Pass the address of your callback in the <i>CallbackRoutine</i> parameter. Pass  <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b> in the <i>NotificationMethod</i> parameter. Retrieve an asynchronous session handle.</li>
<li>Use the asynchronous session handle to call <a href="https://msdn.microsoft.com/61110f24-aa3b-4c51-9205-acac92e03554">WinBioLocateSensor</a>. When the operation finishes, the Windows Biometric Framework will allocate and initialize a  <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure with the results and invoke your callback with a pointer to the results structure.</li>
<li>Call <a href="https://msdn.microsoft.com/b570fc6c-a08e-4485-a621-20f59bd63d40">WinBioFree</a> from your callback implementation to release the <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure after you have finished using it.</li>
</ul>
</div>
<div> </div>



## -parameters




### -param LocateCallbackContext [in, optional]

Pointer to a buffer defined by the application and passed to the <i>LocateCallbackContext</i> parameter of the <a href="https://msdn.microsoft.com/d94db51b-67da-477a-82e6-c92da756f017">WinBioLocateSensorWithCallback</a> function. The buffer is not modified by the framework or the biometric unit. Your application can use the data to help it determine what actions to perform or to maintain additional information about the biometric capture.


### -param OperationStatus [in]

Error code returned by the capture operation.


### -param UnitId

Biometric unit ID number.


## -returns



Do not return a value from your implementation of this function.



