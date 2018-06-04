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

# IDsAdminNewObjPrimarySite::Commit


## -description


The <b>IDsAdminNewObjPrimarySite::Commit</b> method causes a single-page primary object creation extension's <a href="https://msdn.microsoft.com/1788c124-c740-4f77-9687-63113d3b14a8">IDsAdminNewObjExt::WriteData</a> method to be called and writes the temporary object to persistent memory.


## -parameters






## -returns



Returns <b>S_OK</b> if successful or an OLE-defined error code otherwise. This method fails if the calling extension is not a primary object creation extension. This method also fails if the object creation wizard contains more than one page.




## -remarks



The <a href="https://msdn.microsoft.com/ec685ae1-6a37-43d3-84ed-7409611ab63b">IDsAdminNewObjPrimarySite::CreateNew</a> method must be called before <b>IDsAdminNewObjPrimarySite::Commit</b> is called.

When an object creation wizard contains more than one page, the system implements a "Finish" page that displays a summary of the object data to be saved. The system-implemented "Finish" page will perform the  <b>IDsAdminNewObjPrimarySite::Commit</b> operation. If, however, the object creation wizard only contains one page, the  page will have <b>OK</b> and <b>Cancel</b> command buttons instead of the  <b>Back</b>, <b>Next</b> and <b>Cancel</b> buttons normally found in a wizard and no "Finish" page is provided. Because of this, a single-page object creation extension wizard must call <b>Commit</b>.




## -see-also




<a href="https://msdn.microsoft.com/1788c124-c740-4f77-9687-63113d3b14a8">IDsAdminNewObjExt::WriteData</a>



<a href="https://msdn.microsoft.com/cb46cb8f-28ae-44d0-b1de-dc6c090f8fc6">IDsAdminNewObjPrimarySite</a>



<a href="https://msdn.microsoft.com/ec685ae1-6a37-43d3-84ed-7409611ab63b">IDsAdminNewObjPrimarySite::CreateNew</a>
 

 

