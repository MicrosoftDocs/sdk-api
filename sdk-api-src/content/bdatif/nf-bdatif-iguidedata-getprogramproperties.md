---
UID: NF:bdatif.IGuideData.GetProgramProperties
title: IGuideData::GetProgramProperties
author: windows-driver-content
description: The GetProgramProperties method retrieves the properties for a specified program.
old-location: mstv\iguidedata_getprogramproperties.htm
old-project: mstv
ms.assetid: 57eb55bf-49d9-471e-b59c-0d87aa3c3e3c
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetProgramProperties, GetProgramProperties method [Microsoft TV Technologies], GetProgramProperties method [Microsoft TV Technologies],IGuideData interface, IGuideData interface [Microsoft TV Technologies],GetProgramProperties method, IGuideData.GetProgramProperties, IGuideData::GetProgramProperties, IGuideDataGetProgramProperties, bdatif/IGuideData::GetProgramProperties, mstv.iguidedata_getprogramproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdatif.h
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
req.typenames: SmartCardApplication
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdatif.h
api_name:
-	IGuideData.GetProgramProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGuideData::GetProgramProperties


## -description



The <b>GetProgramProperties</b> method retrieves the properties for a specified program.




## -parameters




### -param varProgramDescriptionID [in]

Specifies the unique identifier for the program. Call the <a href="https://msdn.microsoft.com/d182057a-096b-4286-8174-a3ce25c1c86f">IGuideData::GetGuideProgramIDs</a> method to get a list of program identifiers.


### -param ppEnumProperties [out]

Pointer to a variable that receives an <a href="https://msdn.microsoft.com/ae4db426-7e90-4cb6-b53a-2cb7074308fc">IEnumGuideDataProperties</a> interface pointer. Use this interface to enumerate the properties. The caller must release the interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The returned collection includes the following properties.

<table>
<tr>
<th>
              Property
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td>Description.ID</td>
<td>The unique identifier for the program.</td>
</tr>
<tr>
<td>Description.One Sentence</td>
<td>The description of the program.</td>
</tr>
<tr>
<td>Description.Title</td>
<td>The name of the program.</td>
</tr>
</table>
 

The method fails if the TIF has not received the program information from the PSI tables in the transport stream. The client should implement the <a href="https://msdn.microsoft.com/9da565f2-fbcb-4d71-ae40-7d9821f46630">IGuideDataEvent</a> interface and wait for the <a href="https://msdn.microsoft.com/06fcf24b-5d35-4689-9c88-240fe18a46de">IGuideDataEvent::ProgramChanged</a> event to be fired.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3bd27fce-90be-480b-b157-a17beccda068">IGuideData Interface</a>
 

 

