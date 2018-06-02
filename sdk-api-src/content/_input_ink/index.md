---
UID: TP:input_ink
ms.assetid: a4bd3a81-06e5-3941-8e8e-5d06539095d4
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
archived: true
---

# Ink input



Overview of the Ink input technology.

To develop Ink input, you need these headers:

 * [inkpresenterdesktop.h](..\inkpresenterdesktop\index.md)
 * [inkrenderer.h](..\inkrenderer\index.md)

For the programming guide, see [Ink input](/previous-versions/windows/desktop/input_ink).

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IInkCommitRequestHandler interface](..\inkpresenterdesktop\nn-inkpresenterdesktop-iinkcommitrequesthandler.md) | An IInkCommitRequestHandler object enables the app (instead of an IInkPresenterDesktop object) to commit all pending Microsoft DirectComposition commands to the app's DirectComposition visual tree. |
| [IInkD2DRenderer interface](..\inkrenderer\nn-inkrenderer-iinkd2drenderer.md) | An IInkD2DRenderer object enables the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default InkCanvas control. |
| [IInkDesktopHost interface](..\inkpresenterdesktop\nn-inkpresenterdesktop-iinkdesktophost.md) | An IInkDesktopHost object enables ink input, processing, and rendering through the creation of an app thread to host an IInkPresenterDesktop object and insert it into the app's DirectComposition visual tree. |
| [IInkHostWorkItem interface](..\inkpresenterdesktop\nn-inkpresenterdesktop-iinkhostworkitem.md) | An IInkHostWorkItem object represents an ink operation to be executed on an IInkDesktopHost object thread. |
| [IInkPresenterDesktop interface](..\inkpresenterdesktop\nn-inkpresenterdesktop-iinkpresenterdesktop.md) | An IInkPresenterDesktop object represents an InkPresenter that can be configured and inserted into the DirectComposition visual tree of the Classic Windows app. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IInkCommitRequestHandler::OnCommitRequested](..\inkpresenterdesktop\nf-inkpresenterdesktop-iinkcommitrequesthandler-oncommitrequested.md) | Requests that the app commit all pending Microsoft DirectComposition commands to the app's DirectComposition visual tree. |
| [IInkD2DRenderer::Draw](..\inkrenderer\nf-inkrenderer-iinkd2drenderer-draw.md) | Renders the ink stroke to the designated Direct2D device context of the app. |
| [IInkDesktopHost::CreateAndInitializeInkPresenter](..\inkpresenterdesktop\nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter.md) | Creates an IInkPresenterDesktop object on an application thread, connects it to the app's DirectComposition visual tree, and sets the size of the object. |
| [IInkDesktopHost::CreateInkPresenter](..\inkpresenterdesktop\nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter.md) | Creates an IInkPresenterDesktop object on an application thread. |
| [IInkDesktopHost::QueueWorkItem](..\inkpresenterdesktop\nf-inkpresenterdesktop-iinkdesktophost-queueworkitem.md) | Add an ink operation to a work queue for execution on the IInkDesktopHost thread. |
| [IInkHostWorkItem::Invoke](..\inkpresenterdesktop\nf-inkpresenterdesktop-iinkhostworkitem-invoke.md) | Executes the ink operation on an IInkDesktopHost object thread. |
| [IInkPresenterDesktop::GetSize](..\inkpresenterdesktop\nf-inkpresenterdesktop-iinkpresenterdesktop-getsize.md) | Gets the size of the InkPresenter object. |
| [IInkPresenterDesktop::OnHighContrastChanged](..\inkpresenterdesktop\nf-inkpresenterdesktop-iinkpresenterdesktop-onhighcontrastchanged.md) | Specifies a high contrast change handler. This handler is notified of changes to the high contrast system settings. |
| [IInkPresenterDesktop::SetCommitRequestHandler](..\inkpresenterdesktop\nf-inkpresenterdesktop-iinkpresenterdesktop-setcommitrequesthandler.md) | Sets an IInkCommitRequestHandler object that enables the app (instead of an IInkPresenterDesktop object) to commit all pending Microsoft DirectComposition commands to the app's DirectComposition visual tree. |
| [IInkPresenterDesktop::SetRootVisual](..\inkpresenterdesktop\nf-inkpresenterdesktop-iinkpresenterdesktop-setrootvisual.md) | Sets the connection to the app's DirectComposition visual tree. |
| [IInkPresenterDesktop::SetSize](..\inkpresenterdesktop\nf-inkpresenterdesktop-iinkpresenterdesktop-setsize.md) | Sets the size of the InkPresenter object. |
