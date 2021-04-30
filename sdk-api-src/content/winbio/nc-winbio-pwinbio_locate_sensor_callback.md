---
UID: NC:winbio.PWINBIO_LOCATE_SENSOR_CALLBACK
title: PWINBIO_LOCATE_SENSOR_CALLBACK (winbio.h)
description: Returns results from the asynchronous WinBioLocateSensorWithCallback function.
helpviewer_keywords: ["PWINBIO_LOCATE_SENSOR_CALLBACK","PWINBIO_LOCATE_SENSOR_CALLBACK callback","PWINBIO_LOCATE_SENSOR_CALLBACK callback function [Windows Biometric Framework API]","secbiomet.pwinbio_locate_sensor_callback","winbio/PWINBIO_LOCATE_SENSOR_CALLBACK"]
old-location: secbiomet\pwinbio_locate_sensor_callback.htm
tech.root: SecBioMet
ms.assetid: 2959B5C0-A513-4124-8391-E05E9F43CD53
ms.date: 12/05/2018
ms.keywords: PWINBIO_LOCATE_SENSOR_CALLBACK, PWINBIO_LOCATE_SENSOR_CALLBACK callback, PWINBIO_LOCATE_SENSOR_CALLBACK callback function [Windows Biometric Framework API], secbiomet.pwinbio_locate_sensor_callback, winbio/PWINBIO_LOCATE_SENSOR_CALLBACK
req.header: winbio.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PWINBIO_LOCATE_SENSOR_CALLBACK
 - winbio/PWINBIO_LOCATE_SENSOR_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio.h
api_name:
 - PWINBIO_LOCATE_SENSOR_CALLBACK
---

# PWINBIO_LOCATE_SENSOR_CALLBACK callback function


## -description

Called by the Windows Biometric Framework to return results from the   asynchronous  <a href="/windows/desktop/api/winbio/nf-winbio-winbiolocatesensorwithcallback">WinBioLocateSensorWithCallback</a> function. The client application must implement this function.


<div class="alert"><b>Important</b>  We recommend that, beginning with Windows 8, you no longer use the <b>PWINBIO_LOCATE_SENSOR_CALLBACK</b>/<b>WinBioLocateSensorWithCallback</b> combination. Instead, do the following:<ul>
<li>Implement a <a href="/windows/desktop/api/winbio/nc-winbio-pwinbio_async_completion_callback">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function to receive notice when the operation completes.</li>
<li>Call the <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a> function. Pass the address of your callback in the <i>CallbackRoutine</i> parameter. Pass  <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b> in the <i>NotificationMethod</i> parameter. Retrieve an asynchronous session handle.</li>
<li>Use the asynchronous session handle to call <a href="/windows/desktop/api/winbio/nf-winbio-winbiolocatesensor">WinBioLocateSensor</a>. When the operation finishes, the Windows Biometric Framework will allocate and initialize a  <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure with the results and invoke your callback with a pointer to the results structure.</li>
<li>Call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> from your callback implementation to release the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure after you have finished using it.</li>
</ul>
</div>
<div> </div>

## -parameters

### -param LocateCallbackContext [in, optional]

Pointer to a buffer defined by the application and passed to the <i>LocateCallbackContext</i> parameter of the <a href="/windows/desktop/api/winbio/nf-winbio-winbiolocatesensorwithcallback">WinBioLocateSensorWithCallback</a> function. The buffer is not modified by the framework or the biometric unit. Your application can use the data to help it determine what actions to perform or to maintain additional information about the biometric capture.

### -param OperationStatus [in]

Error code returned by the capture operation.

### -param UnitId

Biometric unit ID number.