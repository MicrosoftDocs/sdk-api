---
UID: NN:termmgr.ITPluggableTerminalClassRegistration
title: ITPluggableTerminalClassRegistration
author: windows-sdk-content
description: The ITPluggableTerminalClassRegistration interface exposes methods that allow the creation, modification, and deletion of the registry entry for a pluggable terminal.
old-location: tapi3\itpluggableterminalclassregistration.htm
tech.root: Tapi
ms.assetid: 178824f5-9dda-4e8a-b921-f2c9d064a83c
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITPluggableTerminalClassRegistration, ITPluggableTerminalClassRegistration interface [TAPI 2.2], ITPluggableTerminalClassRegistration interface [TAPI 2.2],described, _tapi3_itpluggableterminalclassregistration, tapi3.itpluggableterminalclassregistration, termmgr/ITPluggableTerminalClassRegistration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: termmgr.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalClassRegistration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPluggableTerminalClassRegistration interface


## -description


The 
<b>ITPluggableTerminalClassRegistration</b> interface exposes methods that allow the creation, modification, and deletion of the registry entry for a pluggable terminal. (Each pluggable terminal must register itself in order to make the terminal available to applications.) The 
<b>ITPluggableTerminalClassRegistration</b> interface is created using COM <b>CoCreateInstance</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPluggableTerminalClassRegistration</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITPluggableTerminalClassRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITPluggableTerminalClassRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e5104e1-5276-4c5b-9a1a-404904432982">Add</a>
</td>
<td align="left" width="63%">
Adds the terminal into the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddc0e33a-d7f4-4380-b53b-e368f7646cbf">Delete</a>
</td>
<td align="left" width="63%">
Deletes the terminal entry from the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/085139b8-3f72-40d5-8323-c6083f06abe7">get_CLSID</a>
</td>
<td align="left" width="63%">
Gets the CLSID used to <b>CoCreateInstance</b> the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fea01c2a-e822-441a-89bc-8607762bc2eb">get_Company</a>
</td>
<td align="left" width="63%">
Gets the name of the company that issued this pluggable terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67f2f241-2389-476f-a412-af456c1c3376">get_Direction</a>
</td>
<td align="left" width="63%">
Gets the direction supported by the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa8c0da8-2953-483a-b3b9-7a6f3e35c893">get_MediaTypes</a>
</td>
<td align="left" width="63%">
Gets the media types supported by the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bbc0862-41d7-40cc-9b9d-57a2238122ee">get_Name</a>
</td>
<td align="left" width="63%">
Gets the terminal's friendly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8da33c46-a369-4501-8249-48ad5d454c58">get_TerminalClass</a>
</td>
<td align="left" width="63%">
Gets the terminal's terminal class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ce4345b-7d8e-4142-a4ee-df1e8b613a25">get_Version</a>
</td>
<td align="left" width="63%">
Gets the terminal version.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35eed68f-be15-4229-b1be-01734f1831c9">GetTerminalClassInfo</a>
</td>
<td align="left" width="63%">
Gets all information from the registry for a specific terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9688cdc7-f55d-41c6-8db7-689617a24239">put_CLSID</a>
</td>
<td align="left" width="63%">
Sets the CLSID used to <b>CoCreateInstance</b> the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e68539dc-0ebe-41f7-a9fe-941e2f941225">put_Company</a>
</td>
<td align="left" width="63%">
Sets the name of the company that issued this pluggable terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b68c0697-e889-471d-857a-d11e974c6552">put_Direction</a>
</td>
<td align="left" width="63%">
Sets the direction supported by the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5a5fb8b-5b71-4f57-8125-46c482897c21">put_MediaTypes</a>
</td>
<td align="left" width="63%">
Sets the media types supported by the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3d6c585-5592-4ed9-80bb-a55ff151edd1">put_Name</a>
</td>
<td align="left" width="63%">
Sets the terminal's friendly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/257adef8-f578-4c8c-9fe9-df59572b7f6e">put_TerminalClass</a>
</td>
<td align="left" width="63%">
Sets the terminal's terminal class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fd659d3-869b-4055-bbd2-e567d13f239d">put_Version</a>
</td>
<td align="left" width="63%">
Sets the terminal version.

</td>
</tr>
</table> 

