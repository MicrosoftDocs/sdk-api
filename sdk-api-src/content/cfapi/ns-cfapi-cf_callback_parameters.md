---
UID: NS:cfapi.CF_CALLBACK_PARAMETERS
title: CF_CALLBACK_PARAMETERS (cfapi.h)
description: Contains callback specific parameters such as file offset, length, flags, etc.
helpviewer_keywords: ["CF_CALLBACK_PARAMETERS","CF_CALLBACK_PARAMETERS structure","cfapi/CF_CALLBACK_PARAMETERS","cloudApi.cf_callback_parameters"]
old-location: cloudapi\cf_callback_parameters.htm
tech.root: cloudapi
ms.assetid: FA403E9E-5EFA-4285-9619-614DB0044FFB
ms.date: 12/05/2018
ms.keywords: CF_CALLBACK_PARAMETERS, CF_CALLBACK_PARAMETERS structure, cfapi/CF_CALLBACK_PARAMETERS, cloudApi.cf_callback_parameters
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CF_CALLBACK_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_CALLBACK_PARAMETERS
 - cfapi/CF_CALLBACK_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_CALLBACK_PARAMETERS
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

The system time when the cloud file in question was dehydrated. It is a count of 100-nanosecond intervals since January 1, 1601.

### -field DUMMYUNIONNAME.FetchData.LastDehydrationReason

A member of the [CF_CALLBACK_DEHYDRATION_REASON](ne-cfapi-cf_callback_dehydration_reason.md) enumeration specifying the reason that the file was last dehydrated.

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

A member of the [CF_CALLBACK_DEHYDRATION_REASON](ne-cfapi-cf_callback_dehydration_reason.md) enumeration specifying the reason why the placeholder is being dehydrated.

### -field DUMMYUNIONNAME.DehydrateCompletion

### -field DUMMYUNIONNAME.DehydrateCompletion.Flags

Placeholder dehydration completion flags.

### -field DUMMYUNIONNAME.DehydrateCompletion.Reason

A member of the [CF_CALLBACK_DEHYDRATION_REASON](ne-cfapi-cf_callback_dehydration_reason.md) enumeration specifying the reason why the placeholder was dehydrated.

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

