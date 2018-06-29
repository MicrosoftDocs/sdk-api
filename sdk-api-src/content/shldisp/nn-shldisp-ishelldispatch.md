---
UID: NN:shldisp.IShellDispatch
title: IShellDispatch
author: windows-sdk-content
description: Represents an object in the Shell.
old-location: shell\IShellDispatch.htm
old-project: shell
ms.assetid: 9B429C03-7F80-45db-B8CD-58D19FAD2E61
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IShellDispatch, IShellDispatch object [Windows Shell], IShellDispatch object [Windows Shell],described, shell.IShellDispatch, shldisp/IShellDispatch
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellDispatch
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch interface


## -description


Represents an object in the Shell. Methods are provided to control the Shell and to execute commands within the Shell. There are also methods to obtain other Shell-related objects.
            
            
<div class="alert"><b>Note</b>  <b>IShellDispatch</b> is implemented and accessed through the <a href="https://msdn.microsoft.com/library/windows/hardware/mt270130">Shell</a> object.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellDispatch</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IShellDispatch</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/578C51C1-F59B-4604-A09B-62BA61225ABB">BrowseForFolder</a>
</td>
<td align="left" width="63%">
Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6A957D70-D6A3-4485-8DF3-7FD2C6DEFF78">CascadeWindows</a>
</td>
<td align="left" width="63%">
Cascades all of the windows on the desktop. This method has the same effect as right-clicking the taskbar and selecting <b>Cascade windows</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9A9B6B3F-FBBC-4e76-8018-8858B6392276">ControlPanelItem</a>
</td>
<td align="left" width="63%">
Runs the specified Control Panel application. If the application is already open, it will activate the running instance.

            

<div class="alert"><b>Note</b>  As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function. To open those Control Panel applications, pass the canonical name to control.exe. For example:

                <pre class="syntax" xml:space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34448D82-187C-40aa-90B4-A4111B33048B">EjectPC</a>
</td>
<td align="left" width="63%">
Ejects the computer from its docking station. This is the same as clicking the <b>Start</b> menu and selecting <b>Eject PC</b>, if your computer supports this command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DB434D02-56B2-4e8f-9E43-BBF47C7BE377">Explore</a>
</td>
<td align="left" width="63%">
Opens a specified folder in a Windows Explorer window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BC7C4C26-593D-4467-A2AA-4F2DF835C989">FileRun</a>
</td>
<td align="left" width="63%">
Displays the <b>Run</b> dialog to the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9B687A8A-BB29-49a0-8AE3-11A75FAF3257">FindComputer</a>
</td>
<td align="left" width="63%">
Displays the <b>Search Results: Computers</b> dialog box. The dialog box shows the result of the search for a specified computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6F588D5E-5B6E-4000-BAD5-B557FB975FCA">FindFiles</a>
</td>
<td align="left" width="63%">
Displays the <b>Find: All Files</b> dialog box. This is the same as clicking the <b>Start</b> menu and then selecting <b>Search</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926862">Help</a>
</td>
<td align="left" width="63%">
Displays the Windows Help and Support window. This method has the same effect as clicking the <b>Start</b> menu and selecting <b>Help and Support</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25DD56B0-221E-44a2-9FAD-FB358ADD7FF1">MinimizeAll</a>
</td>
<td align="left" width="63%">
Minimizes all of the windows on the desktop. This method has the same effect as right-clicking the taskbar and selecting <b>Minimize All Windows</b> on older systems or clicking the <b>Show Desktop</b> icon on the taskbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CEA73705-1C27-4138-86C4-1715016E2ED8">NameSpace</a>
</td>
<td align="left" width="63%">
Creates and returns a <a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a> object for the specified folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</td>
<td align="left" width="63%">
Opens the specified folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D36FA5A0-AF03-4627-86E0-869BF1440958">RefreshMenu</a>
</td>
<td align="left" width="63%">
Refreshes the contents of the <b>Start</b> menu. Used only with systems preceding Windows XP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D4B949F6-5508-4624-9706-491184703DC6">SetTime</a>
</td>
<td align="left" width="63%">
Displays the <b>Date and Time</b> dialog box. This method has the same effect as right-clicking the clock in the taskbar status area and selecting <b>Adjust date/time</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3C4F6579-6398-4af4-8911-FE22555B0ABC">ShutdownWindows</a>
</td>
<td align="left" width="63%">
Displays the <b>Shut Down Windows</b> dialog box. This is the same as clicking the <b>Start</b> menu and selecting <b>Shut Down</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927278">Suspend</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85785510-6B75-450a-A9BB-6C3B4F6194E2">TileHorizontally</a>
</td>
<td align="left" width="63%">
Tiles all of the windows on the desktop horizontally. This method has the same effect as right-clicking the taskbar and selecting <b>Show windows stacked</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63CB7E20-48E6-4cfe-B0BA-0D28A7B151BD">TileVertically</a>
</td>
<td align="left" width="63%">
Tiles all of the windows on the desktop vertically. This method has the same effect as right-clicking the taskbar and selecting <b>Show windows side by side</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8E0AC08E-1132-4312-9B75-E7686B91AB02">TrayProperties</a>
</td>
<td align="left" width="63%">
Displays the <b>Taskbar and Start Menu Properties</b> dialog box. This method has the same effect as right-clicking the taskbar and selecting <b>Properties</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32BDE544-C4FF-4a64-99AF-F8960AEC4690">UndoMinimizeALL</a>
</td>
<td align="left" width="63%">
Restores all desktop windows to the state they were in before the last <a href="https://msdn.microsoft.com/3af98a16-27d1-4c93-ac72-7c9e24e68c23">MinimizeAll</a> command. This method has the same effect as right-clicking the taskbar and selecting <b>Undo Minimize All Windows</b> (on older systems) or a second clicking of the <b>Show Desktop</b> icon in the taskbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/mt637455">Windows</a>
</td>
<td align="left" width="63%">
Creates and returns a <a href="https://msdn.microsoft.com/cad1f961-7fb4-4ba1-be48-b664d3de2c60">ShellWindows</a> object. This object represents a collection of all of the open windows that belong to the Shell.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellDispatch</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/jj159071">Application</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains an object that represents an application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2FDEF8D3-3F5B-43ae-9812-83B4249D9CBB">Parent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an object that represents the parent of the current object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/75fc151e-5b9e-476b-b4e5-b848917357a8">Shell Object</a>
 

 

