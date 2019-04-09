---
UID: NS:winioctl._CSV_QUERY_REDIRECT_STATE
title: CSV_QUERY_REDIRECT_STATE (winioctl.h)
author: windows-sdk-content
description: Contains information about whether files in a stream have been redirected.
old-location: fs\csv_query_redirect_state.htm
tech.root: FileIO
ms.assetid: E628FFC2-B665-4160-AA63-9F027D4A2736
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCSV_QUERY_REDIRECT_STATE, CSV_QUERY_REDIRECT_STATE, CSV_QUERY_REDIRECT_STATE structure [Files], PCSV_QUERY_REDIRECT_STATE, PCSV_QUERY_REDIRECT_STATE structure pointer [Files], fs.csv_query_redirect_state, winioctl/CSV_QUERY_REDIRECT_STATE, winioctl/PCSV_QUERY_REDIRECT_STATE"
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - CSV_QUERY_REDIRECT_STATE
product: Windows
targetos: Windows
req.typenames: CSV_QUERY_REDIRECT_STATE, *PCSV_QUERY_REDIRECT_STATE
req.redist: 
---

# CSV_QUERY_REDIRECT_STATE structure


## -description


Contains information about whether files in a stream have been redirected.


## -struct-fields




### -field MdsNodeId

The identifier of an MDS node.


### -field DsNodeId

The identifier of a DS node.


### -field FileRedirected

<b>TRUE</b> if the file has been redirected; otherwise, 
      <b>FALSE</b>.


## -remarks



This structure is used if the <a href="https://msdn.microsoft.com/6CCCD5CA-FF29-41D4-B687-E403CADABF84">FSCTL_CSV_CONTROL</a> 
    control code is called with a <a href="https://msdn.microsoft.com/77A2106F-2C07-4A30-BA46-651F74032609">CSV_CONTROL_OP</a> enumeration 
    value of <b>CsvControlQueryRedirectState</b>, or if the control code is used with an 
    <a href="https://msdn.microsoft.com/B984F8CA-3548-4442-8D3B-B2F469F699E1">CSV_CONTROL_PARAM</a> structure containing that enumeration 
    value.




## -see-also




<a href="https://msdn.microsoft.com/77A2106F-2C07-4A30-BA46-651F74032609">CSV_CONTROL_OP</a>



<a href="https://msdn.microsoft.com/B984F8CA-3548-4442-8D3B-B2F469F699E1">CSV_CONTROL_PARAM</a>



<a href="https://msdn.microsoft.com/6CCCD5CA-FF29-41D4-B687-E403CADABF84">FSCTL_CSV_CONTROL</a>



<a href="https://msdn.microsoft.com/406d5c0f-b49a-4075-ac3e-c5b55a0c3fe9">File Management Structures</a>
 

 

