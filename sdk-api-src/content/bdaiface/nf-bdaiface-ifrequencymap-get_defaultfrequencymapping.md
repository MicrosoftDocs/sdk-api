---
UID: NF:bdaiface.IFrequencyMap.get_DefaultFrequencyMapping
title: IFrequencyMap::get_DefaultFrequencyMapping
author: windows-sdk-content
description: The get_DefaultFrequencyMapping method returns the default frequency table for a given country/region code.
old-location: mstv\ifrequencymap_get_defaultfrequencymapping.htm
old-project: mstv
ms.assetid: 67057c70-cb4d-4828-ad97-cf0181bd8cfe
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IFrequencyMap interface [Microsoft TV Technologies],get_DefaultFrequencyMapping method, IFrequencyMap.get_DefaultFrequencyMapping, IFrequencyMap::get_DefaultFrequencyMapping, IFrequencyMapget_DefaultMapping, bdaiface/IFrequencyMap::get_DefaultFrequencyMapping, get_DefaultFrequencyMapping, get_DefaultFrequencyMapping method [Microsoft TV Technologies], get_DefaultFrequencyMapping method [Microsoft TV Technologies],IFrequencyMap interface, mstv.ifrequencymap_get_defaultfrequencymapping
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IFrequencyMap.get_DefaultFrequencyMapping
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IFrequencyMap::get_DefaultFrequencyMapping


## -description



The <b>get_DefaultFrequencyMapping</b> method returns the default frequency table for a given country/region code. This method returns the frequency table, but does not set the country/region code on Network Provider. The Network Provider continues to use the same frequency table it was using before the method was called.




## -parameters




### -param ulCountryCode [in]

Specifies the country/region code.


### -param pulCount [out]

Pointer to a variable that receives the size of the frequency table.


### -param ppulList [out]

Pointer to a variable that receives the address of the frequency table. The frequency table is an array of size <i>pulCount</i>, allocated by the method. The caller must free the array by calling <b>CoTaskMemFree</b>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Each entry in the frequency table is a tuning frequency, in kilohertz (kHz).

For a list of country/region codes, see <a href="https://msdn.microsoft.com/a71784eb-e6b4-4dab-91fc-103c39dd1591">Country/Region Assignments</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0f7f1b2c-a191-45f5-a645-367e898b6ee2">IFrequencyMap Interface</a>
 

 

