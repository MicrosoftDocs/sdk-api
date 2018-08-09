---
UID: NS:werapi._WER_REPORT_INFORMATION
title: "_WER_REPORT_INFORMATION"
author: windows-sdk-content
description: Contains information used by the WerReportCreate function.
old-location: wer\wer_report_information.htm
old-project: wer
ms.assetid: 3efe2b43-53ac-48e3-bc39-4a9fe6041fca
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PWER_REPORT_INFORMATION, PWER_REPORT_INFORMATION, PWER_REPORT_INFORMATION structure pointer [Windows Error Reporting], WER_REPORT_INFORMATION, WER_REPORT_INFORMATION structure [Windows Error Reporting], _WER_REPORT_INFORMATION, base.wer_report_information, wer.wer_report_information, werapi/PWER_REPORT_INFORMATION, werapi/WER_REPORT_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: WER_REPORT_INFORMATION, *PWER_REPORT_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Werapi.h
api_name:
 - WER_REPORT_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WER_REPORT_INFORMATION structure


## -description


Contains information used by the <a href="https://msdn.microsoft.com/41f68dde-5e43-45a6-8e0b-3ae0c6180e8b">WerReportCreate</a> function.


## -struct-fields




### -field dwSize

The size of this structure, in bytes.


### -field hProcess

A handle to the process for which the report is being generated. If this member is <b>NULL</b>, this is the calling process.


### -field wzConsentKey

The name used to look up consent settings. If this member is empty, the default is the name specified by the <i>pwzEventType</i> parameter of <a href="https://msdn.microsoft.com/41f68dde-5e43-45a6-8e0b-3ae0c6180e8b">WerReportCreate</a>.


### -field wzFriendlyEventName

The display name. If this member is empty, the default is the name specified by <i>pwzEventType</i> parameter of <a href="https://msdn.microsoft.com/41f68dde-5e43-45a6-8e0b-3ae0c6180e8b">WerReportCreate</a>.


### -field wzApplicationName

The name of the application. If this parameter is empty, the default is the base name of the image file.


### -field wzApplicationPath

The full path to the application.


### -field wzDescription

A description of the problem. This description is displayed in <b>Problem Reports and Solutions</b> on Windows Vista or the problem reports pane of the <b>Action Center</b> on Windows 7.


### -field hwndParent

A handle to the parent window.


## -see-also




<a href="https://msdn.microsoft.com/41f68dde-5e43-45a6-8e0b-3ae0c6180e8b">WerReportCreate</a>
 

 

