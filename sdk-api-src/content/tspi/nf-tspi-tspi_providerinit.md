---
UID: NF:tspi.TSPI_providerInit
title: TSPI_providerInit function (tspi.h)
description: The TSPI_providerInit function initializes the service provider and gives it parameters required for subsequent operations.
helpviewer_keywords: ["TSPI_providerInit","TSPI_providerInit function [TAPI 2.2]","_tspi_tspi_providerinit","tspi.tspi_providerinit","tspi/TSPI_providerInit"]
old-location: tspi\tspi_providerinit.htm
tech.root: tapi3
ms.assetid: 6cb7817b-6df3-4a6a-a666-b41c2eb0b118
ms.date: 12/05/2018
ms.keywords: TSPI_providerInit, TSPI_providerInit function [TAPI 2.2], _tspi_tspi_providerinit, tspi.tspi_providerinit, tspi/TSPI_providerInit
req.header: tspi.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TSPI_providerInit
 - tspi/TSPI_providerInit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_providerInit
---

# TSPI_providerInit function


## -description

The 
<b>TSPI_providerInit</b> function initializes the service provider and gives it parameters required for subsequent operations.

## -parameters

### -param dwTSPIVersion

The version of the TSPI definition under which this function must operate. The caller can use 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiatetspiversion">TSPI_lineNegotiateTSPIVersion</a> with the special <i>dwDeviceID</i>
<a href="/windows/desktop/Tapi/initialize-negotiation">INITIALIZE_NEGOTIATION</a> to negotiate a version that is guaranteed to be acceptable to the service provider.

### -param dwPermanentProviderID

The permanent identifier, unique within the service providers on this system, of the service provider being initialized.

### -param dwLineDeviceIDBase

The lowest device identifier for the line devices supported by this service provider.

### -param dwPhoneDeviceIDBase

The lowest device identifier for the phone devices supported by this service provider.

### -param dwNumLines

The number of line devices this service provider supports. The value returned is the number of line devices reported in 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerenumdevices">TSPI_providerEnumDevices</a>.

### -param dwNumPhones

The number of phone devices this service provider supports. The value returned is the number of phone devices reported in 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerenumdevices">TSPI_providerEnumDevices</a>.

### -param lpfnCompletionProc

The procedure the service provider calls to report completion of all asynchronously operating procedures on line and phone devices.

### -param lpdwTSPIOptions

A pointer to a <b>DWORD</b>-sized memory location, into which the service provider can write a value specifying LINETSPIOPTIONS_ values. This parameter allows the service provider to return bits indicating optional behaviors desired of TAPI. TAPI sets the options <b>DWORD</b> to 0 before calling 
<b>TSPI_providerInit</b>, so if the service provider doesn't want any of these options, it can just leave the <b>DWORD</b> set to 0. 




At this time, only one bit is defined to be returned through this pointer: LINETSPIOPTION_NONREENTRANT. The service provider sets this bit if it is not designed for fully preemptive, multithreaded, multitasking, multiprocessor operation (for example, updating of global data protected by mutexes). When this bit is set, TAPI only makes one call at a time to the service provider; it does not call any other entry point, nor that entry point again, until the service provider returns from the original function call. Without this bit set, TAPI may call into multiple service provider entry points, including multiple times to the same entry point, simultaneously (actually simultaneously in a multiprocessor system).

<div class="alert"><b>Note</b>  <b>Important:</b> It must be emphasized that setting this bit degrades performance. It is strongly recommended that this be used only for development but not a shipped production service provider.</div>
<div> </div>
TAPI does not serialize access to TSPI functions that display a dialog box (
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_lineconfigdialog">TUISPI_lineConfigDialog</a>, 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_lineconfigdialogedit">TUISPI_lineConfigDialogEdit</a>, 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_phoneconfigdialog">TUISPI_phoneConfigDialog</a>, 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerconfig">TUISPI_providerConfig</a>, 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerinstall">TUISPI_providerInstall</a>, 
<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerremove">TUISPI_providerRemove</a>) so that they do not block other TSPI functions from being called; the service provider must include internal protection on these functions.

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_INIFILECORRUPT, LINEERR_NOMULTIPLEINSTANCE.

## -remarks

This function is guaranteed to be called before any of the other functions prefixed with <b>TSPI_line</b> or <b>TSPI_phone</b> except 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiatetspiversion">TSPI_lineNegotiateTSPIVersion</a>. It is strictly paired with a subsequent call to 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providershutdown">TSPI_providerShutdown</a> These pairs may overlap, for example, when the Telephony Control Panel utility supplied with Windows Telephony in versions 1.4 and earlier is used while telephony operations are in progress. The call to this function must be ignored (returning success) if there is already an outstanding pair.

A service provider should perform as many consistency checks as is practical at the time. 
<b>TSPI_providerInit</b> is called to ensure that it is ready to run. Some consistency or installation errors, however, cannot be detected until the operation is attempted. The error LINEERR_NODRIVER can be used to report such nonspecific errors at the time they are detected.

There is no directly corresponding function at the TAPI level. At that level, multiple different usage instances can be outstanding, with an "application handle" returned to identify the instance in subsequent operations. At TSPI level, the interface architecture supports only a single usage instance for each distinct service provider.

## -see-also

<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiatetspiversion">TSPI_lineNegotiateTSPIVersion</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providershutdown">TSPI_providerShutdown</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_lineconfigdialog">TUISPI_lineConfigDialog</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_lineconfigdialogedit">TUISPI_lineConfigDialogEdit</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_phoneconfigdialog">TUISPI_phoneConfigDialog</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerconfig">TUISPI_providerConfig</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerinstall">TUISPI_providerInstall</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tuispi_providerremove">TUISPI_providerRemove</a>