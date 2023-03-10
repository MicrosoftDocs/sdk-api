---
UID: NF:fsrmpipeline.IFsrmPropertyDefinition.get_ValueDescriptions
title: IFsrmPropertyDefinition::get_ValueDescriptions (fsrmpipeline.h)
description: Descriptions for each of the possible values specified in the PossibleValues property. (Get)
helpviewer_keywords: ["IFsrmPropertyDefinition interface [File Server Resource Manager]","ValueDescriptions property","IFsrmPropertyDefinition.ValueDescriptions","IFsrmPropertyDefinition.get_ValueDescriptions","IFsrmPropertyDefinition::ValueDescriptions","IFsrmPropertyDefinition::get_ValueDescriptions","IFsrmPropertyDefinition::put_ValueDescriptions","ValueDescriptions property [File Server Resource Manager]","ValueDescriptions property [File Server Resource Manager]","IFsrmPropertyDefinition interface","fs.ifsrmpropertydefinition_valuedescriptions","fsrm.ifsrmpropertydefinition_valuedescriptions","fsrmpipeline/IFsrmPropertyDefinition::ValueDescriptions","fsrmpipeline/IFsrmPropertyDefinition::get_ValueDescriptions","fsrmpipeline/IFsrmPropertyDefinition::put_ValueDescriptions","get_ValueDescriptions"]
old-location: fsrm\ifsrmpropertydefinition_valuedescriptions.htm
tech.root: fsrm
ms.assetid: 3c6a9457-c1bb-4bc3-853a-3676bb4ce6bb
ms.date: 12/05/2018
ms.keywords: IFsrmPropertyDefinition interface [File Server Resource Manager],ValueDescriptions property, IFsrmPropertyDefinition.ValueDescriptions, IFsrmPropertyDefinition.get_ValueDescriptions, IFsrmPropertyDefinition::ValueDescriptions, IFsrmPropertyDefinition::get_ValueDescriptions, IFsrmPropertyDefinition::put_ValueDescriptions, ValueDescriptions property [File Server Resource Manager], ValueDescriptions property [File Server Resource Manager],IFsrmPropertyDefinition interface, fs.ifsrmpropertydefinition_valuedescriptions, fsrm.ifsrmpropertydefinition_valuedescriptions, fsrmpipeline/IFsrmPropertyDefinition::ValueDescriptions, fsrmpipeline/IFsrmPropertyDefinition::get_ValueDescriptions, fsrmpipeline/IFsrmPropertyDefinition::put_ValueDescriptions, get_ValueDescriptions
req.header: fsrmpipeline.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmPropertyDefinition::get_ValueDescriptions
 - fsrmpipeline/IFsrmPropertyDefinition::get_ValueDescriptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmPropertyDefinition.ValueDescriptions
 - IFsrmPropertyDefinition.get_ValueDescriptions
 - IFsrmPropertyDefinition.put_ValueDescriptions
---

# IFsrmPropertyDefinition::get_ValueDescriptions


## -description

Descriptions for each of the possible values specified in the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertydefinition-get_possiblevalues">PossibleValues</a> 
    property.

This property is read/write.

## -parameters

## -remarks

There is a one-to-one relationship between these descriptions and the list of possible values specified in the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertydefinition-get_possiblevalues">PossibleValues</a> property. If you 
    do not want to specify a description for one of the values in the list, set the corresponding item in the array to 
    an empty string.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpropertydefinition">IFsrmPropertyDefinition</a>
