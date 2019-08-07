---
UID: NE:winioctl._CSV_CONTROL_OP
title: CSV_CONTROL_OP
author: windows-sdk-content
description: Specifies the type of CSV control operation to use with the FSCTL_CSV_CONTROL control code.
old-location: fs\csv_control_op.htm
tech.root: FileIO
ms.assetid: 77A2106F-2C07-4A30-BA46-651F74032609
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PCSV_CONTROL_OP, CSV_CONTROL_OP, CSV_CONTROL_OP enumeration [Files], CsvControlMdsPath, CsvControlQueryFileRevision, CsvControlQueryRedirectState, CsvControlStartRedirectFile, CsvControlStopRedirectFile, PCSV_CONTROL_OP, PCSV_CONTROL_OP enumeration pointer [Files], fs.csv_control_op, winioctl/CSV_CONTROL_OP, winioctl/CsvControlMdsPath, winioctl/CsvControlQueryFileRevision, winioctl/CsvControlQueryRedirectState, winioctl/CsvControlStartRedirectFile, winioctl/CsvControlStopRedirectFile, winioctl/PCSV_CONTROL_OP'
ms.topic: enum
f1_keywords:
- winioctl/CSV_CONTROL_OP
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
- CSV_CONTROL_OP
product: Windows
targetos: Windows
req.typenames: CSV_CONTROL_OP, *PCSV_CONTROL_OP
req.redist: 
---

# CSV_CONTROL_OP enumeration


## -description


Specifies the type of CSV control operation to use with the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_csv_control">FSCTL_CSV_CONTROL</a> control code.


## -enum-fields




### -field CsvControlStartRedirectFile

Start file redirection.


### -field CsvControlStopRedirectFile

Stop file redirection.


### -field CsvControlQueryRedirectState

Search for state redirection. When this value is specified, the 
      <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-csv_query_redirect_state">CSV_QUERY_REDIRECT_STATE</a> structure must also 
      be used.


### -field CsvControlQueryFileRevision

Search for file revision. When this value is specified, the 
      <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-csv_query_file_revision">CSV_QUERY_FILE_REVISION</a> structure must also be 
      used.


### -field CsvControlQueryMdsPath


### -field CsvControlQueryFileRevisionFileId128


### -field CsvControlQueryVolumeRedirectState


### -field CsvControlEnableUSNRangeModificationTracking


### -field CsvControlMarkHandleLocalVolumeMount


### -field CsvControlUnmarkHandleLocalVolumeMount


### -field CsvControlGetCsvFsMdsPathV2


### -field CsvControlDisableCaching


### -field CsvControlEnableCaching




#### - CsvControlMdsPath

Search for MDS path. When this value is specified, the 
      <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-csv_query_mds_path">CSV_QUERY_MDS_PATH</a> structure must also be used.


## -remarks



An alternative to calling the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_csv_control">FSCTL_CSV_CONTROL</a> 
    control code with this enumeration is to use the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-csv_control_param">CSV_CONTROL_PARAM</a> structure, which encapsulates a member 
    of this enumeration type.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-csv_control_param">CSV_CONTROL_PARAM</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-csv_query_file_revision">CSV_QUERY_FILE_REVISION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-csv_query_mds_path">CSV_QUERY_MDS_PATH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-csv_query_redirect_state">CSV_QUERY_REDIRECT_STATE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_csv_control">FSCTL_CSV_CONTROL</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-enumerations">File Management Enumerations</a>
 

 

