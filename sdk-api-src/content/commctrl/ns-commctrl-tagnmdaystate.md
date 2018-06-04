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

# tagNMDAYSTATE structure


## -description


Carries information required to process the <a href="https://msdn.microsoft.com/dc2608e0-c598-4b26-9195-208f09cd84b7">MCN_GETDAYSTATE</a> notification code. All members of this structure are for input, except 
			<b>prgDayState</b>, which the receiving application must set when processing MCN_GETDAYSTATE. 


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about this notification code. 


### -field stStart

Type: <b><a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a></b>


<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the starting date. 


### -field cDayState

Type: <b>int</b>

INT value specifying the total number of elements that must be in the array at 
					<b>prgDayState</b>. 


### -field prgDayState

Type: <b>LPMONTHDAYSTATE</b>

Address of an array of <a href="https://msdn.microsoft.com/eb3dd6cb-738e-424b-945b-1485798a444c">MONTHDAYSTATE</a> values. The buffer at this address must be large enough to contain at least 
					<b>cDayState</b> elements. The first element in the array corresponds to the date in 
					<b>stStart</b>. 

