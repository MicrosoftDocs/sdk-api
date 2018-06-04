---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# FWPM_FILTER_CONDITION0_ structure


## -description


The <b>FWPM_FILTER_CONDITION0</b> structure expresses a filter condition that must be true for the action to be taken.


## -struct-fields




### -field fieldKey

GUID of the field to be tested.


### -field matchType

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff552437">FWP_MATCH_TYPE</a> value that specifies the type of match to be performed.


### -field conditionValue

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a> structure that contains the value to match the field against.


## -remarks



Field GUIDs are
   only unique within a layer, so both the field GUID and the layer GUID are required to uniquely identify a
   field.

The data type of 
<b>conditionValue</b> must be compatible with the <b>matchType</b> value. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552437">FWP_MATCH_TYPE</a> for detailed  compatibility rules.

<b>FWPM_FILTER_CONDITION0</b> is a specific implementation of FWPM_FILTER_CONDITION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.


#### Examples

The following C++ example shows how to initialize and add conditions to a filter.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;fwpmu.h&gt;
#include &lt;stdio.h&gt;

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
    result = FwpmGetAppIdFromFileName0(FILE0_PATH, &amp;fwpApplicationByteBlob);
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
      memset(&amp;fwpFilter, 0, sizeof(FWPM_FILTER0));

      fwpFilter.numFilterConditions = conCount;
      if (conCount &gt; 0)
        fwpFilter.filterCondition = fwpConditions;

      // Finish initializing filter...

    return;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552437">FWP_MATCH_TYPE</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

