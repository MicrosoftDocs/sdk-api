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

# IShellPropSheetExt::AddPages


## -description


Adds one or more pages to a property sheet that the Shell displays for a file object. The Shell calls this method for each property sheet handler registered to the file type.


## -parameters




### -param pfnAddPage [in]

Type: <b>LPFNADDPROPSHEETPAGE</b>

A pointer to a function that the property sheet handler calls to add a page to the property sheet. The function takes a property sheet handle returned by the <a href="https://msdn.microsoft.com/fb7ca67a-7dff-4e1d-a303-5da87d8bbd2b">CreatePropertySheetPage</a> function and the <i>lParam</i> parameter passed to this method.


### -param lParam [in]

Type: <b>LPARAM</b>

Handler-specific data to pass to the function pointed to by <i>pfnAddPage</i>.


## -returns



Type: <b>HRESULT</b>

If successful, returns a one-based index to specify the page that should be initially displayed. See Remarks for more information.
                




## -remarks



For each page that the property sheet handler needs to add to a property sheet, the handler fills a <a href="https://msdn.microsoft.com/69ceb9f4-f68c-4c60-9610-4c1977aae4b8">PROPSHEETPAGE</a> structure, calls the <a href="https://msdn.microsoft.com/fb7ca67a-7dff-4e1d-a303-5da87d8bbd2b">CreatePropertySheetPage</a> function, and then calls the function pointed to by <i>pfnAddPage</i>.

The <b>LPFNADDPROPSHEETPAGE</b> function pointer type is defined in Prsht.h as shown here. It accepts a handle to a <a href="https://msdn.microsoft.com/69ceb9f4-f68c-4c60-9610-4c1977aae4b8">PROPSHEETPAGE</a> structure and function-defined data through <i>lParam</i>.

                

<pre class="syntax" xml:space="preserve"><code>typedef BOOL (* LPFNADDPROPSHEETPAGE)(HPROPSHEETPAGE, LPARAM);</code></pre>
You can request through your implementation that a particular property sheet page be displayed first, instead of the default page. To do so, return the one-based index of the desired page relative to the pages you added. For example, if you added three property sheet pages, A, B, and C, and you want B to be the selected page, then the return value should be 2. Note that this return value is only a request. The property sheet might still display the default page.



