---
UID: NF:bdatif.IGuideData.GetGuideProgramIDs
title: IGuideData::GetGuideProgramIDs
author: windows-driver-content
description: The GetGuideProgramIDs method returns a list of unique identifiers for all of the programs contained in all transport streams.
old-location: mstv\iguidedata_getguideprogramids.htm
old-project: mstv
ms.assetid: d182057a-096b-4286-8174-a3ce25c1c86f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetGuideProgramIDs, GetGuideProgramIDs method [Microsoft TV Technologies], GetGuideProgramIDs method [Microsoft TV Technologies],IGuideData interface, IGuideData interface [Microsoft TV Technologies],GetGuideProgramIDs method, IGuideData.GetGuideProgramIDs, IGuideData::GetGuideProgramIDs, IGuideDataGetGuideProgramIDs, bdatif/IGuideData::GetGuideProgramIDs, mstv.iguidedata_getguideprogramids
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
-	IGuideData.GetGuideProgramIDs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGuideData::GetGuideProgramIDs


## -description



The <b>GetGuideProgramIDs</b> method returns a list of unique identifiers for all of the programs contained in all transport streams.




## -parameters




### -param pEnumPrograms






#### - ppEnumPrograms [out]

Receives a pointer to the <b>IEnumVARIANT</b> interface. Use this interface to enumerate the collection. The caller must release the interface.


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



The method fails if the TIF has not received the program information from the PSI tables in the transport stream. The client should implement the <a href="https://msdn.microsoft.com/9da565f2-fbcb-4d71-ae40-7d9821f46630">IGuideDataEvent</a> interface and wait for the <a href="https://msdn.microsoft.com/06fcf24b-5d35-4689-9c88-240fe18a46de">IGuideDataEvent::ProgramChanged</a> event to be fired.

Each <b>VARIANT</b> type in the collection contains a <b>BSTR</b> that uniquely identifies one program within the multiplex. To get more information about the program, pass the <b>VARIANT</b> to the <a href="https://msdn.microsoft.com/57eb55bf-49d9-471e-b59c-0d87aa3c3e3c">IGuideData::GetProgramProperties</a> method.

The returned <b>IEnumVARIANT</b> interface is not thread safe. Clients should not call methods on the interface from more than one thread.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3bd27fce-90be-480b-b157-a17beccda068">IGuideData Interface</a>
 

 

