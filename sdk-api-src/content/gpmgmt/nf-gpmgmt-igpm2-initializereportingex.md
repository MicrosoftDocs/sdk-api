---
UID: NF:gpmgmt.IGPM2.InitializeReportingEx
title: IGPM2::InitializeReportingEx (gpmgmt.h)
description: Sets the location to search for .adm files and the reporting option to determine whether to include comments in the report. This method initializes reporting in an asynchronous manner.
helpviewer_keywords: ["IGPM2 interface [GPMC]","InitializeReportingEx method","IGPM2.InitializeReportingEx","IGPM2::InitializeReportingEx","InitializeReportingEx","InitializeReportingEx method [GPMC]","InitializeReportingEx method [GPMC]","IGPM2 interface","gpmc.igpm2_initializereportingex","gpmgmt/IGPM2::InitializeReportingEx"]
old-location: gpmc\igpm2_initializereportingex.htm
tech.root: gpmc
ms.assetid: 3de74745-d9b3-47a7-8ba7-08b4e57d2ab7
ms.date: 12/05/2018
ms.keywords: IGPM2 interface [GPMC],InitializeReportingEx method, IGPM2.InitializeReportingEx, IGPM2::InitializeReportingEx, InitializeReportingEx, InitializeReportingEx method [GPMC], InitializeReportingEx method [GPMC],IGPM2 interface, gpmc.igpm2_initializereportingex, gpmgmt/IGPM2::InitializeReportingEx
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPM2::InitializeReportingEx
 - gpmgmt/IGPM2::InitializeReportingEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gpmgmt.dll
api_name:
 - IGPM2.InitializeReportingEx
---

# IGPM2::InitializeReportingEx


## -description

Sets the location to search for .adm files and the reporting option to determine whether to include comments in the report. This method initializes reporting in an asynchronous manner.

For both Group Policy object (GPO) reporting or Resultant Set of Policy (RSOP) reporting, the Group Policy Management Console (GPMC) searches for and loads .adm files in the following order. First it searches for the specified .adm files in the specified location. Then it searches for any additional .adm files in the default location. Finally it searches the GPO or RSoP for any additional .adm files.

## -parameters

### -param bstrAdmPath [in]

Location to search for .adm files.

### -param reportingOptions [in]

Reporting options. This parameter must be one of the following values.



#### 0

Do not include comments in the report.



#### 1

Include comments in the report.

## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm2">IGPM2</a>