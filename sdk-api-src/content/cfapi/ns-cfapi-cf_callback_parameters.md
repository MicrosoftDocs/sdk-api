---
UID: NS:cfapi.CF_CALLBACK_PARAMETERS
title: CF_CALLBACK_PARAMETERS
author: windows-sdk-content
description: Contains callback specific parameters such as file offset, length, flags, etc.
old-location: cloudapi\cf_callback_parameters.htm
old-project: cfApi
ms.assetid: FA403E9E-5EFA-4285-9619-614DB0044FFB
ms.author: windowssdkdev
ms.date: 02/27/2018
ms.keywords: CF_CALLBACK_PARAMETERS, CF_CALLBACK_PARAMETERS structure, cfapi/CF_CALLBACK_PARAMETERS, cloudApi.cf_callback_parameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: CF_CALLBACK_PARAMETERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_CALLBACK_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CF_CALLBACK_PARAMETERS structure


## -description


Contains callback specific parameters such as file offset, length, flags, etc.


## -struct-fields




### -field ParamSize

 


### -field DUMMYUNIONNAME


### -field DUMMYUNIONNAME.Cancel


### -field DUMMYUNIONNAME.Cancel.Flags

Cancel data flags.


### -field DUMMYUNIONNAME.Cancel.DUMMYUNIONNAME


### -field DUMMYUNIONNAME.Cancel.DUMMYUNIONNAME.FetchData


### -field DUMMYUNIONNAME.Cancel.DUMMYUNIONNAME.FetchData.FileOffset

Offset, in bytes, for specifying the range of data.


### -field DUMMYUNIONNAME.Cancel.DUMMYUNIONNAME.FetchData.Length

Length of the data in bytes.


### -field DUMMYUNIONNAME.FetchData


### -field DUMMYUNIONNAME.FetchData.Flags

Fetch data flags.


### -field DUMMYUNIONNAME.FetchData.RequiredFileOffset

Offset, in bytes, for specifying the required range of data.


### -field DUMMYUNIONNAME.FetchData.RequiredLength

Length of the required data to retrieve, in bytes.


### -field DUMMYUNIONNAME.FetchData.OptionalFileOffset

Offset, in bytes, of a broader piece of data to provide to a sync provider. This is optional and can be used if the sync provider prefers to work with larger segments of data.


### -field DUMMYUNIONNAME.FetchData.OptionalLength

Length, in bytes, of a broader piece of data to provide to a sync provider. This is optional and can be used if the sync provider prefers to work with larger segments of data.


### -field DUMMYUNIONNAME.FetchData.LastDehydrationTime

 


### -field DUMMYUNIONNAME.FetchData.LastDehydrationReason

 


### -field DUMMYUNIONNAME.ValidateData


### -field DUMMYUNIONNAME.ValidateData.Flags

Data validation flags.


### -field DUMMYUNIONNAME.ValidateData.RequiredFileOffset

Offset, in bytes, for specifying the range of data to validate.


### -field DUMMYUNIONNAME.ValidateData.RequiredLength

Length, in bytes, of the data to validate.


### -field DUMMYUNIONNAME.FetchPlaceholders


### -field DUMMYUNIONNAME.FetchPlaceholders.Flags

Flags for fetching placeholder metadata.


### -field DUMMYUNIONNAME.FetchPlaceholders.Pattern

 A standard Windows file pattern which may contain wildcard characters (‘?’, ‘*’). All placeholders information matching the pattern must be transferred, but not necessarily in one-shot, as a minimum requirement. Alternatively, a sync provider may choose to   not transfer placeholders matching the pattern.


### -field DUMMYUNIONNAME.OpenCompletion


### -field DUMMYUNIONNAME.OpenCompletion.Flags

Placeholder open completion flags.


### -field DUMMYUNIONNAME.CloseCompletion


### -field DUMMYUNIONNAME.CloseCompletion.Flags

Placeholder close completion flags.


### -field DUMMYUNIONNAME.Dehydrate


### -field DUMMYUNIONNAME.Dehydrate.Flags

Placeholder dehydration flags.


### -field DUMMYUNIONNAME.Dehydrate.Reason

 


### -field DUMMYUNIONNAME.DehydrateCompletion

 


### -field DUMMYUNIONNAME.DehydrateCompletion.Flags

 


### -field DUMMYUNIONNAME.DehydrateCompletion.Reason

 


### -field DUMMYUNIONNAME.Delete


### -field DUMMYUNIONNAME.Delete.Flags

Placeholder deletion flags.


### -field DUMMYUNIONNAME.DeleteCompletion


### -field DUMMYUNIONNAME.DeleteCompletion.Flags

Placeholder deletion complete flags.


### -field DUMMYUNIONNAME.Rename


### -field DUMMYUNIONNAME.Rename.Flags

Rename placeholder flags.


### -field DUMMYUNIONNAME.Rename.TargetPath

The full rename/move target path relative to the volume.


### -field DUMMYUNIONNAME.RenameCompletion


### -field DUMMYUNIONNAME.RenameCompletion.Flags

Rename completion placeholder flags.


### -field DUMMYUNIONNAME.RenameCompletion.SourcePath

The full source link path relative to the volume.

