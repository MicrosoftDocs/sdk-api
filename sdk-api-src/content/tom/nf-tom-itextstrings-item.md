---
UID: NF:tom.ITextStrings.Item
title: ITextStrings::Item (tom.h)
author: windows-sdk-content
description: Gets an ITextRange2 object for a selected index in a string collection.
old-location: controls\itextstrings_item.htm
tech.root: Controls
ms.assetid: 8eed4bc6-75a8-440e-a334-543e7b996df0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextStrings interface [Windows Controls],Item method, ITextStrings.Item, ITextStrings::Item, Item, Item method [Windows Controls], Item method [Windows Controls],ITextStrings interface, controls.itextstrings_item, tom/ITextStrings::Item
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextStrings.Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStrings::Item


## -description


Gets an <a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a> object for a selected index in a string collection.


## -parameters




### -param Index [in]

Type: <b>long</b>

The index of the string to retrieve. The default value is 1.


### -param ppRange [out, retval]

Type: <b><a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>**</b>

The object to receive the range.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The first string corresponds to Index = 1 and the last to Count which is given by <a href="https://msdn.microsoft.com/6bbe53ab-bd03-4445-8d36-0186a43da451">ITextStrings_GetCount</a>.




## -see-also




<a href="https://msdn.microsoft.com/c878d0db-ac13-4ac9-8601-d1c1ba76cd85">ITextStrings</a>
 

 

