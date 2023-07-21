---
UID: NF:bdatif.IGuideData.GetProgramProperties
title: IGuideData::GetProgramProperties (bdatif.h)
description: The GetProgramProperties method retrieves the properties for a specified program.
helpviewer_keywords: ["GetProgramProperties","GetProgramProperties method [Microsoft TV Technologies]","GetProgramProperties method [Microsoft TV Technologies]","IGuideData interface","IGuideData interface [Microsoft TV Technologies]","GetProgramProperties method","IGuideData.GetProgramProperties","IGuideData::GetProgramProperties","IGuideDataGetProgramProperties","bdatif/IGuideData::GetProgramProperties","mstv.iguidedata_getprogramproperties"]
old-location: mstv\iguidedata_getprogramproperties.htm
tech.root: mstv
ms.assetid: 57eb55bf-49d9-471e-b59c-0d87aa3c3e3c
ms.date: 12/05/2018
ms.keywords: GetProgramProperties, GetProgramProperties method [Microsoft TV Technologies], GetProgramProperties method [Microsoft TV Technologies],IGuideData interface, IGuideData interface [Microsoft TV Technologies],GetProgramProperties method, IGuideData.GetProgramProperties, IGuideData::GetProgramProperties, IGuideDataGetProgramProperties, bdatif/IGuideData::GetProgramProperties, mstv.iguidedata_getprogramproperties
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGuideData::GetProgramProperties
 - bdatif/IGuideData::GetProgramProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IGuideData.GetProgramProperties
---

# IGuideData::GetProgramProperties


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetProgramProperties</b> method retrieves the properties for a specified program.

## -parameters

### -param varProgramDescriptionID [in]

Specifies the unique identifier for the program. Call the <a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getguideprogramids">IGuideData::GetGuideProgramIDs</a> method to get a list of program identifiers.

### -param ppEnumProperties [out]

Pointer to a variable that receives an <a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-ienumguidedataproperties">IEnumGuideDataProperties</a> interface pointer. Use this interface to enumerate the properties. The caller must release the interface.

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
<th>Property
            </th>
<th>Description
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
 

The method fails if the TIF has not received the program information from the PSI tables in the transport stream. The client should implement the <a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedataevent">IGuideDataEvent</a> interface and wait for the <a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedataevent-programchanged">IGuideDataEvent::ProgramChanged</a> event to be fired.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedata">IGuideData Interface</a>