---
UID: NS:fwpmtypes.FWPM_FILTER_CONDITION0_
title: FWPM_FILTER_CONDITION0 (fwpmtypes.h)
description: Expresses a filter condition that must be true for the action to be taken.
helpviewer_keywords: ["FWPM_FILTER_CONDITION0","FWPM_FILTER_CONDITION0 structure [Filtering]","fwp.fwpm_filter_condition0_struct","fwpmtypes/FWPM_FILTER_CONDITION0"]
old-location: fwp\fwpm_filter_condition0_struct.htm
tech.root: fwp
ms.assetid: 4dfed9d7-e51b-425c-9f27-014229c140be
ms.date: 12/05/2018
ms.keywords: FWPM_FILTER_CONDITION0, FWPM_FILTER_CONDITION0 structure [Filtering], fwp.fwpm_filter_condition0_struct, fwpmtypes/FWPM_FILTER_CONDITION0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_FILTER_CONDITION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_FILTER_CONDITION0_
 - fwpmtypes/FWPM_FILTER_CONDITION0_
 - FWPM_FILTER_CONDITION0
 - fwpmtypes/FWPM_FILTER_CONDITION0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_FILTER_CONDITION0
---

# FWPM_FILTER_CONDITION0 structure


## -description

The <b>FWPM_FILTER_CONDITION0</b> structure expresses a filter condition that must be true for the action to be taken.

## -struct-fields

### -field fieldKey

GUID of the field to be tested. The available keys are listed under [Filtering Condition Identifiers](/windows/win32/fwp/filtering-condition-identifiers-).

### -field matchType


A [FWP_MATCH_TYPE](https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_match_type) value that specifies the type of match to be performed.


### -field conditionValue

A [FWP_CONDITION_VALUE0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_condition_value0) structure that contains the value to match the field against.



## -remarks

Field GUIDs are
   only unique within a layer, so both the field GUID and the layer GUID are required to uniquely identify a
   field.

The data type of 

[FWP_MATCH_TYPE](https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_match_type) for detailed  compatibility rules.


<b>FWPM_FILTER_CONDITION0</b> is a specific implementation of FWPM_FILTER_CONDITION. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.


#### Examples

The following C++ example shows how to initialize and add conditions to a filter.


```cpp
#include <windows.h>
#include <fwpmu.h>
#include <stdio.h>

#pragma comment(lib, "Fwpuclnt.lib")

// Some application to use for filter testing.
#define FILE0_PATH L"C:\\Program Files\\AppDirectory\\SomeApplication.exe"

void main()
{
    FWP_BYTE_BLOB *fwpApplicationByteBlob;
    FWPM_FILTER0 fwpFilter;
    FWPM_FILTER_CONDITION0 fwpConditions[4];
    int conCount = 0;
    DWORD result = ERROR_SUCCESS; 

    fwpApplicationByteBlob = (FWP_BYTE_BLOB*) malloc(sizeof(FWP_BYTE_BLOB));
    
    printf("Retrieving application identifier for filter testing.\n"); 
    result = FwpmGetAppIdFromFileName0(FILE0_PATH, &fwpApplicationByteBlob);
    if (result != ERROR_SUCCESS)
    {
        printf("FwpmGetAppIdFromFileName failed (%d).\n", result);
        return;
    }

      // Application identifier filter condition.
      fwpConditions[conCount].fieldKey = FWPM_CONDITION_ALE_APP_ID;
      fwpConditions[conCount].matchType = FWP_MATCH_EQUAL;
      fwpConditions[conCount].conditionValue.type = FWP_BYTE_BLOB_TYPE;
      fwpConditions[conCount].conditionValue.byteBlob = fwpApplicationByteBlob;
            
      ++conCount;

      // TCP protocol filter condition
      fwpConditions[conCount].fieldKey = FWPM_CONDITION_IP_PROTOCOL;
      fwpConditions[conCount].matchType = FWP_MATCH_EQUAL;
      fwpConditions[conCount].conditionValue.type = FWP_UINT8;
      fwpConditions[conCount].conditionValue.uint8 = IPPROTO_TCP;

      ++conCount;

      // Add conditions and condition count to a filter.
      memset(&fwpFilter, 0, sizeof(FWPM_FILTER0));

      fwpFilter.numFilterConditions = conCount;
      if (conCount > 0)
        fwpFilter.filterCondition = fwpConditions;

      // Finish initializing filter...

    return;
}

```

## -see-also

[FWP_CONDITION_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_condition_value0)



[FWP_MATCH_TYPE](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_match_type)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>