---
UID: NF:tspi.TSPI_lineConfigDialog
title: TSPI_lineConfigDialog function
author: windows-sdk-content
description: The TSPI_lineConfigDialog function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement TUISPI_lineConfigDialog.
old-location: tspi\tspi_lineconfigdialog.htm
old-project: tapi
ms.assetid: b0f26029-ddb2-472c-8a09-2abf213dab16
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: TSPI_lineConfigDialog, TSPI_lineConfigDialog function [TAPI 2.2], _tspi_tspi_lineconfigdialog, tspi.tspi_lineconfigdialog, tspi/TSPI_lineConfigDialog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: AAAccountingData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineConfigDialog
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_lineConfigDialog function


## -description


The 
<b>TSPI_lineConfigDialog</b> function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement 
<a href="https://msdn.microsoft.com/405af7aa-eb0b-49a1-9712-2f86357fc720">TUISPI_lineConfigDialog</a>.

The 
<b>TSPI_lineConfigDialog</b> function causes the provider of the specified line device to display a modal dialog box as a child window of <i>hwndOwner</i> to allow the user to configure parameters related to the line device.


## -parameters




### -param dwDeviceID

The line device to be configured.


### -param hwndOwner

A handle to a parent window in which the dialog box window is to be placed.


### -param lpszDeviceClass

A pointer to a <b>null</b>-terminated Unicode string that identifies a device class name. This device class allows the caller to select a specific subscreen of configuration information applicable to that device class. If this parameter is <b>NULL</b> or an empty string, the highest level configuration dialog box should be selected. The permitted strings are the same as for 
<a href="https://msdn.microsoft.com/d4331721-61c3-4de0-bb1f-c27f475170d1">TSPI_lineGetID</a>. For example, if the line supports the Comm API, passing comm/datamodem as <i>lpszDeviceClass</i> causes the provider to display the parameters related specifically to Comm (or, at least, to start at the corresponding point in a multilevel configuration dialog box chain, so that the user doesn't have to search to find the desired parameters.)


## -returns



Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INUSE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALDEVICECLASS, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.




## -remarks



The procedure must update the [Windows Telephony] section in the Win.ini file and broadcast the WM_WININICHANGE message if it makes any changes to the Telephon.ini file that would cause a change in the line or address capabilities reported in 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a> or 
<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a>, or if a line device is created or removed.

There is no restriction that this function (<b>TSPI_lineConfigDialog</b>) be called only when the line is closed. However, each provider can impose such a restriction itself. When 
<b>TSPI_lineConfigDialog</b> is called, the provider could alert the user with the message "The line is in use by one or more applications. You may not change the line configuration while the line is in use" (and return the error message LINEERR_INUSE). However, some configuration may be safe to change "on the fly," particularly those related to media types (such as the modem error control protocol), especially when that media type is not currently in use. The provider could allow those options to be changed while the line is open.

Users should not be allowed to change anything that alters values returned with 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a> or 
<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a> without first forcibly closing the line as a signal that applications must call functions that return these structures in order to have accurate information.




## -see-also




<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a>



<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/87307bc6-0c0e-41d0-bc88-2d806214c13e">TSPI_lineGetDevConfig</a>



<a href="https://msdn.microsoft.com/d4331721-61c3-4de0-bb1f-c27f475170d1">TSPI_lineGetID</a>



<a href="https://msdn.microsoft.com/41699ca8-a30d-48ab-bace-bc2b95b67e77">TSPI_lineSetDevConfig</a>
 

 

