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

# WBEMTime::SetDMTF


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetDMTF</b> method sets the time in the <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> object. The time is given by its <b>BSTR</b> parameter in Date and Time Format. A date and time argument earlier than midnight January 1, 1601 is not valid.


## -parameters




### -param wszText

<b>BSTR</b> in <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a>.


## -returns



The method returns <b>true</b> if the time is valid and <b>false</b> if the time is not valid.




## -remarks



Internally, <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> stores a datetime as a 64-bit integer. Because of this, implementation-specific interpretation to the use of an asterisk is required when setting a datetime.

When an asterisk "*" appears in any location in the inbound datetime string, <i>wszText</i> is replaced on a positional basis with the default datetime string "16010101000000.000000+000".

The microsecond separator "." and UTC offset sign "+/-" must be present in the correct locations. All other positions are replaced by the default element if an asterisk is detected in the corresponding location.

For example, "1979**********.000000-0*4" becomes "197910101000000.000000-004".

Because <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> internally stores all datetime values in GMT, the resulting UTC of -004 causes the minute field to change so that the internal representation becomes "197910105000000.000000+000".




## -see-also




<a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a>



<a href="https://msdn.microsoft.com/f1fe92cc-1d51-4bd7-950b-84c76b001163">WBEMTime::GetBSTR</a>



<a href="https://msdn.microsoft.com/3bfcf7f8-0b0c-4a3f-83c7-be4c37753a7a">WBEMTime::GetDMTF</a>
 

 

